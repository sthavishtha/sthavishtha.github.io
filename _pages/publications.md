---
layout: page
permalink: /publications/
title: Publications
description: "* indicates corresponding author(s)"
years: [2026, 2024, 2023, 2022, 2021, 2020, 2019, 2018]
nav: true
nav_order: 2
topics:
  - Multiphase flows
  - Fluid-structure interaction
  - Porous media
  - Isogeometric analysis
  - Lattice Boltzmann methods
---

<!-- _pages/publications.md -->

<div class="theme-lead" markdown="1">
Research areas: `multiphase flows`, `fluid-structure interaction`, `porous media`, `isogeometric analysis` and `lattice Boltzmann methods`.
</div>

<div class="pub-filter" id="pub-filter" role="group" aria-label="Filter publications by research area">
  <button type="button" class="pub-filter-btn active" data-topic="all">All</button>
  {%- for topic in page.topics %}
    <button type="button" class="pub-filter-btn" data-topic="{{ topic | downcase }}">{{ topic }}</button>
  {%- endfor %}
</div>

<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>

<script>
  // Filter the publication list by the keywords already rendered on each entry.
  document.addEventListener("DOMContentLoaded", function () {
    const filter = document.getElementById("pub-filter");
    if (!filter) return;

    const buttons = Array.from(filter.querySelectorAll(".pub-filter-btn"));
    const entries = Array.from(document.querySelectorAll(".publications ol.bibliography > li")).map(function (item) {
      const keywords = Array.from(item.querySelectorAll(".keyword")).map(function (kw) {
        return kw.textContent.trim().toLowerCase();
      });
      return { item: item, keywords: keywords };
    });

    function matches(entry, topic) {
      return topic === "all" || entry.keywords.indexOf(topic) !== -1;
    }

    buttons.forEach(function (button) {
      const topic = button.dataset.topic;
      const count = entries.filter(function (entry) {
        return matches(entry, topic);
      }).length;
      if (count === 0) {
        button.hidden = true;
        return;
      }
      button.insertAdjacentHTML("beforeend", ' <span class="pub-filter-count">' + count + "</span>");
    });

    function apply(topic) {
      entries.forEach(function (entry) {
        entry.item.style.display = matches(entry, topic) ? "" : "none";
      });
      // Hide the year heading of any group left with nothing to show.
      document.querySelectorAll(".publications ol.bibliography").forEach(function (list) {
        const visible = Array.from(list.children).some(function (item) {
          return item.style.display !== "none";
        });
        list.style.display = visible ? "" : "none";
        const heading = list.previousElementSibling;
        if (heading && heading.classList.contains("year")) {
          heading.style.display = visible ? "" : "none";
        }
      });
    }

    filter.addEventListener("click", function (event) {
      const button = event.target.closest(".pub-filter-btn");
      if (!button) return;
      buttons.forEach(function (other) {
        other.classList.toggle("active", other === button);
      });
      apply(button.dataset.topic);
    });
  });
</script>
