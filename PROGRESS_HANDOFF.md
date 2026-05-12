# Progress Handoff

## 1. Goal

Convert the personal academic website at `sthavishtha.github.io` from the al-folio demo/template state into a fully personalized site for **Sthavishtha Bhopalam Rajakumar** (PhD Candidate, Mechanical Engineering, Purdue University). The site should mirror the clean academic style of `sbryngelson.github.io/academic-website-template` while preserving al-folio's Jekyll/Liquid infrastructure.

---

## 2. Files Modified and Why

### Content & Configuration

| File | Change | Reason |
|------|--------|--------|
| `_config.yml` | `baseurl:` set to empty; `scholar.last_name/first_name` set; `max_author_limit:` cleared; `keyword` + `data` added to `filtered_bibtex_keywords` | Personal GitHub Pages site needs empty baseurl; author highlight requires name match; show all co-authors; enable custom bib fields |
| `_data/socials.yml` | `email`, `scholar_userid: 1xy4ycEAAAAJ`, `github_username`, `orcid_id` set; `rss_icon: false` | Populate real social links; enable Google Scholar badge; remove RSS icon |
| `_pages/about.md` | Subtitle, circular profile photo, advisor/education sidebar, real bio text, Flag Counter widget at bottom | Match sbryngelson template style; show education inline without a separate CV page |
| `_pages/publications.md` | `years:` list set to `[2026, 2024, 2023, 2022, 2021, 2020, 2019, 2018]` | Matches actual publication years |
| `_pages/blog.md`, `repositories.md`, `teaching.md`, `profiles.md`, `cv.md`, `dropdown.md` | `nav: false` | Remove unused demo pages from navigation |
| `_bibliography/papers.bib` | Replaced all demo entries with 11 real publications; added `keyword`, `data`, `google_scholar_id`, `preview`, `altmetric`, `arxiv`, `bibtex_show` fields to each | Populate real publication list with all metadata needed for badges and buttons |
| `_news/announcement_1,2,3.md` | Updated with real news items (fibrotaxis preprint, CMAME paper, Physics of Fluids featured article) | Replace al-folio placeholder announcements |

### Layout & Styling

| File | Change | Reason |
|------|--------|--------|
| `_layouts/bib.liquid` | Title linked to DOI/arXiv; content column `col-sm-9`; image column `col-sm-3 text-center`; row uses `align-items-center`; `sizes="260px"`; periodical simplified (year removed); `additional_info` rendered as separate div; keywords split on comma into multiple badges; `Data` button added after arXiv | Match desired publications page style: colored linked titles, no year after journal, italic additional info, multi-keyword badges, data repository button, larger centered preview images |
| `_sass/_publications.scss` | `h2.bibliography { display: none; }`; `.title a` colored; `.keyword.btn` filled/non-clickable; `.additional-info` italic + light color; `.preview` set to `display: block; width: 100%` with centered image | Remove auto-generated year headings/dividers; style titles, keywords, and additional info; ensure preview images fill and center within their column |

### CI / Automation

| File | Change | Reason |
|------|--------|--------|
| `.github/workflows/update-citations.yml` | `timeout 90` → `timeout 300` | 90s was too short for scholarly to fetch 11+ papers; was causing exit code 124 |
| `bin/update_scholar_citations.py` | Added `from scholarly import ProxyGenerator`; replaced invalid `scholarly.use_proxy(backend="free_proxies")` with `pg = ProxyGenerator(); pg.FreeProxies(); scholarly.use_proxy(pg)`; `set_timeout(15)` → `set_timeout(30)` | GitHub Actions IP ranges are blocked by Google Scholar; free proxy rotation bypasses this; longer per-request timeout accounts for proxy latency |

---

## 3. Unresolved Bugs / Blockers

### Critical: `_data/citations.yml` has wrong data
- **Problem:** `_data/citations.yml` exists and was last updated `2026-05-01`, but it was populated from the al-folio demo Scholar profile (`qc6CJjYAAAAJ` — Einstein), not from Sthavishtha's profile (`1xy4ycEAAAAJ`). This means citation counts shown on the publications page are wrong (or missing for Sthavishtha's papers).
- **Fix:** Re-run the GitHub Actions workflow now that `scholar_userid` is correctly set to `1xy4ycEAAAAJ`. Go to **Actions → Update Google Scholar Citations → Run workflow**. The `FreeProxies` fix is in place; if the workflow still fails, see "Next Steps" below.

### Unstable: Free proxy reliability
- **Problem:** `scholarly`'s `FreeProxies()` backend is unreliable — it cycles through public proxies that may be slow or dead. The workflow may succeed or fail non-deterministically.
- **Fix options (in order of preference):**
  1. **ScraperAPI** (recommended): Free tier gives 1,000 requests/month. Sign up at `scraperapi.com`, get an API key, add it as a GitHub Actions secret `SCRAPER_API_KEY`, then replace `pg.FreeProxies()` with `pg.ScraperAPI('YOUR_KEY')` in `bin/update_scholar_citations.py`.
  2. Keep retrying manually via `workflow_dispatch` until a free proxy works (usually succeeds within 2–3 tries).

### Minor: `email` field in `_data/socials.yml` is commented out
- The line `# email: sthavishtha@purdue.edu` is commented out. Uncomment it to display the email icon in the social links footer.

---

## 4. Immediate Next Steps (Next Session)

1. **Fix citations.yml** — Trigger the GitHub Actions workflow (`Actions → Update Google Scholar Citations → Run workflow`) and verify it completes successfully. If it fails again, implement ScraperAPI as described above.

2. **Verify Google Scholar badges** — After citations.yml is regenerated with `1xy4ycEAAAAJ` data, confirm the scholar citation count badges on the publications page show correct numbers for Sthavishtha's papers.

3. **Uncomment email in `_data/socials.yml`** — Remove the `#` from `# email: sthavishtha@purdue.edu`.

4. **Add missing preview images** — Not all bib entries have a `preview` field. Currently only `bhopalam2026droplet` (`dropmob.png`) and `bhopalam2026simulating` (`pinchoff.png`) have previews. Consider adding `preview = {filename.png}` to `bhopalam2024fibrotaxis`, `bhopalam2022elastocapillary`, and others, and placing images in `assets/img/publication_preview/`.

5. **Add `compddrop.png` to bib** — The file `assets/img/publication_preview/compddrop.png` exists but is not referenced in any bib entry. Likely belongs to `bhopalam2022elastocapillary` (compound droplets paper).

6. **LinkedIn / ResearchGate** — Fill in `linkedin_username` and/or `researchgate_username` in `_data/socials.yml` if desired.

7. **Projects page** — `_pages/projects.md` still has demo al-folio content. Update or set `nav: false` if not needed.

8. **ClustrMaps** — The about page currently uses a Flag Counter widget. If a ClustrMaps map is preferred instead (shows visitor locations on a world map), replace the Flag Counter `<img>` tag with the ClustrMaps script obtained by registering the site at `clustrmaps.com/add`.
