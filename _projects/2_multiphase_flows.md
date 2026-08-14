---
layout: page
title: Mechanics of multiphase flows
description: pore-scale physics of sea ice and dry snow, resolved with phase-field simulations
img: assets/img/publication_preview/pinchoff.png
importance: 2
category: research
related_publications: true
_styles: >
  .theme-lead {
    border-left: 3px solid var(--global-theme-color);
    padding-left: 1rem;
    margin: 1.5rem 0 2rem 0;
    font-size: 1.05rem;
  }
  .media-placeholder {
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    min-height: 220px;
    padding: 1.5rem;
    border: 2px dashed var(--global-divider-color);
    border-radius: 8px;
    color: var(--global-text-color-light);
    font-size: 0.9rem;
    letter-spacing: 0.02em;
  }
---

## Sea ice physics

<div class="theme-lead" markdown="1">
Sea ice is not a solid block — at the pore scale it is a multiphase porous material threaded by brine channels that grow, merge, and close as the ice evolves.
</div>

At the pore scale, sea ice is a multiphase porous material composed of interconnected brine channels that evolve in time and space. Existing sea-ice growth models operating at geophysical or Darcy scales treat sea ice as a homogenized medium and neglect its evolving microstructure. However, a pore-scale description of sea ice is essential because its evolution is governed by a two-way coupling between microstructure and brine transport: changes in brine-channel morphology alter local transport properties, while fluid flow and salt redistribution further modify melting, freezing, and brine-channel connectivity. Here, we aim to fundamentally understand the mechanisms governing sea-ice microstructural evolution. Our pore-scale simulations will help formulate improved melt-rate and brine-transport parameterizations for large-scale ocean models {% cite bhopalam2026tbd1 %}.

<div class="row justify-content-sm-center mt-4">
  <div class="col-sm-6 mt-3 mt-md-0">
    <!-- {% raw %}{% include figure.liquid loading="eager" path="assets/img/seaice.png" class="img-fluid rounded z-depth-1" %}{% endraw %} -->
    <div class="media-placeholder">image &mdash; brine-channel microstructure</div>
  </div>
  <div class="col-sm-6 mt-3 mt-md-0">
    <!-- {% raw %}{% include video.liquid path="assets/video/seaice.mp4" class="img-fluid rounded z-depth-1" controls=true muted=true loop=true %}{% endraw %} -->
    <div class="media-placeholder">video &mdash; brine transport and channel evolution</div>
  </div>
</div>
<div class="caption">Pore-scale structure of sea ice and its evolution under coupled brine transport and phase change.</div>

---

## Dry snow metamorphism

<div class="theme-lead" markdown="1">
In ice-sediment mixtures, vapor quietly rearranges the ice itself — migrating, coarsening, and aggregating within the pore space, with no liquid involved.
</div>

Ice-sediment mixtures are commonly found in terrestrial permafrost and extraterrestrial regolith. Under dry conditions, spatiotemporal variations in temperature and vapor pressure cause the redistribution of ice within the pore spaces of these mixtures, leading to ice migration, coarsening, and aggregation. These processes strongly influence the long-term stability of subsurface ice. Here, we aim to develop a mechanistic understanding of these pore-scale processes using phase-field simulations {% cite bhopalam2026tbd3 %}.

<div class="row justify-content-sm-center mt-4">
  <div class="col-sm-10 mt-3 mt-md-0">
    <!-- {% raw %}{% include video.liquid path="assets/video/drysnow.mp4" class="img-fluid rounded z-depth-1" controls=true muted=true loop=true %}{% endraw %} -->
    <div class="media-placeholder">video &mdash; vapor-driven ice migration and coarsening</div>
  </div>
</div>
<div class="caption">Phase-field simulation of dry snow metamorphism in an ice-sediment mixture.</div>
