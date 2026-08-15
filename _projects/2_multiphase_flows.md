---
layout: page
title: Mechanics of multiphase flows
description: Applications: cryo-hydrological porous media
img: assets/img/publication_preview/pinchoff.png
importance: 2
category: research
related_publications: false
_styles: >
  .publications ol.bibliography li .col-sm-3 {
    display: none;
  }
  .publications ol.bibliography li .col-sm-9 {
    flex: 0 0 100%;
    max-width: 100%;
  }
  .video-pair video {
    width: 100%;
    height: auto;
    box-shadow: none;
    border: none;
    border-radius: 0;
  }
  .video-pair figure {
    margin: 0;
  }
  @media (min-width: 768px) {
    .video-pair > div:first-child {
      padding-right: 1.75rem;
    }
    .video-pair > div:last-child {
      padding-left: 1.75rem;
    }
  }
  .video-pair .caption {
    margin-top: 0.4rem;
    font-size: 0.85rem;
  }
---

## Sea ice physics

At the pore scale, sea ice is a `multiphase porous material` composed of interconnected brine channels that evolve in time and space. Existing sea-ice growth models operating at geophysical or Darcy scales treat sea ice as a homogenized medium and neglect its evolving microstructure. However, a pore-scale description of sea ice is essential because its evolution is governed by a two-way coupling between microstructure and brine transport -- changes in brine-channel morphology alter local transport properties, while `fluid flow and salt redistribution` further modify `melting, freezing, and brine-channel connectivity`. Here, we aim to fundamentally understand the mechanisms governing sea-ice microstructural evolution. Our `pore-scale` simulations will help formulate improved melt-rate and brine-transport parameterizations for large-scale ocean models.

<div class="row justify-content-sm-center align-items-end mt-4 video-pair">
  <div class="col-md-6 mt-3 mt-md-0">
    {% include video.liquid path="assets/video/seaicemicrostructure.mp4" class="img-fluid" controls=true autoplay=true loop=true muted=true playsinline=true nodownload=true %}
    <div class="caption">Microstructural evolution of sea ice at the ice-ocean boundary during top-down freezing. Video credit: Junning Liu.</div>
  </div>
  <div class="col-md-6 mt-3 mt-md-0">
    {% include video.liquid path="assets/video/seaiceconvection.mp4" class="img-fluid" controls=true autoplay=true loop=true muted=true playsinline=true nodownload=true %}
    <div class="caption">Buoyancy-driven convective transport of brine during interfacial melting of sea ice. Video credit: Junning Liu. </div>
  </div>
</div>

---

## Dry snow metamorphism

Ice-sediment mixtures are commonly found in `terrestrial permafrost` and `extraterrestrial regolith`. Under dry conditions, spatiotemporal variations in temperature and vapor pressure cause the redistribution of ice within the pore spaces of these mixtures, leading to `ice migration, coarsening, and aggregation`. These processes strongly influence the long-term stability of subsurface ice. Here, we aim to develop a mechanistic understanding of these `pore-scale` processes using `phase-field` simulations.

<div class="row justify-content-sm-center mt-4 video-pair">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include video.liquid path="assets/video/dsm.mp4" class="img-fluid" controls=true autoplay=true loop=true muted=true playsinline=true nodownload=true %}
    <div class="caption">Pore-scale simulation of vapor-driven ice migration and coarsening in a tortuous pore space. Video credit: Jackson Baglino.</div>
  </div>
</div>

---

## References

<div class="publications">
  {% bibliography --query @*[key=bhopalam2026tbd1] %}
  {% bibliography --query @*[key=bhopalam2026tbd3] %}
</div>
