---
layout: page
title: Mechanics of multiphase flows
description: pore-scale physics of sea ice and dry snow, resolved with phase-field simulations
img: assets/img/publication_preview/pinchoff.png
importance: 2
category: research
related_publications: false
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

At the pore scale, sea ice is a multiphase porous material composed of interconnected brine channels that evolve in time and space. Existing sea-ice growth models operating at geophysical or Darcy scales treat sea ice as a homogenized medium and neglect its evolving microstructure. However, a pore-scale description of sea ice is essential because its evolution is governed by a two-way coupling between microstructure and brine transport -- changes in brine-channel morphology alter local transport properties, while fluid flow and salt redistribution further modify melting, freezing, and brine-channel connectivity. Here, we aim to fundamentally understand the mechanisms governing sea-ice microstructural evolution. Our pore-scale simulations will help formulate improved melt-rate and brine-transport parameterizations for large-scale ocean models.

<div class="row justify-content-sm-center mt-4">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include video.liquid path="assets/video/seaiceconvection.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true loop=true muted=true playsinline=true %}
  </div>
</div>
<div class="caption">Pore-scale structure of sea ice and its evolution under coupled brine transport and phase change.</div>

---

## Dry snow metamorphism

Ice-sediment mixtures are commonly found in terrestrial permafrost and extraterrestrial regolith. Under dry conditions, spatiotemporal variations in temperature and vapor pressure cause the redistribution of ice within the pore spaces of these mixtures, leading to ice migration, coarsening, and aggregation. These processes strongly influence the long-term stability of subsurface ice. Here, we aim to develop a mechanistic understanding of these pore-scale processes using phase-field simulations.

<div class="row justify-content-sm-center mt-4">
  <div class="col-sm-10 mt-3 mt-md-0">
    <!-- {% raw %}{% include video.liquid path="assets/video/drysnow.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true loop=true muted=true playsinline=true %}{% endraw %} -->
    <div class="media-placeholder">video &mdash; vapor-driven ice migration and coarsening</div>
  </div>
</div>
<div class="caption">Phase-field simulation of dry snow metamorphism in an ice-sediment mixture.</div>
