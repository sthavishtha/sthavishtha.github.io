---
layout: page
title: Multiphase flows
img: assets/img/publication_preview/pinchoff.png
importance: 2
category: research
related_publications: false
_styles: >
  .reference-list {
    counter-reset: refnum;
  }
  .reference-list ol.bibliography {
    list-style: none;
    padding-left: 2rem;
    margin: 0;
  }
  .reference-list ol.bibliography li {
    position: relative;
    margin-bottom: 0.6rem;
    line-height: 1.5;
  }
  .reference-list ol.bibliography li::before {
    counter-increment: refnum;
    content: counter(refnum) ".";
    position: absolute;
    left: -2rem;
    width: 1.5rem;
    text-align: right;
  }
  .reference-list .reference {
    font-size: 0.95rem;
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

<div class="theme-lead" markdown="1">
I have used `computational multiphase flow` models to develop a fundamental understanding of the interfacial phenomena arising from coupled fluid flow, phase change, chemical reactions and heat transfer in the following applications: `cryo-hydrology`, `environmental sustainability` and `combustion and propulsion` systems. My interest in `cryo-hydrological` systems is motivated by the rapid transformation of cryospheric environments, such as `snowpacks`, `glaciers`, and `permafrost`, under changing climatic conditions. My interest in `environmentally sustainable` applications is driven by the need to address growing global water scarcity. My interest in `combustion and propulsion systems` is motivated by the need to improve energy efficiency, and emissions performance in next-generation energy and transportation technologies.
</div>

## Sea ice physics

At the `pore-scale`, sea ice is a `multiphase porous material` composed of interconnected brine channels that evolve in time and space. The spatiotemporal evolution of the sea ice microstructure is governed by a two-way coupling with brine transport - changes in brine-channel morphology alter local transport properties, while `fluid flow and salt redistribution` modify `melting`, `freezing`, and `brine-channel connectivity`. Despite the importance of these `pore-scale` processes, existing sea-ice growth models operate at geophysical or Darcy scales, and neglect the evolving microstructure of sea ice. Here, we aim to fundamentally understand the mechanisms governing sea-ice microstructural evolution through `pore-scale` simulations. Our simulations will help formulate improved melt-rate and brine-transport parameterizations for large-scale ocean models.

<div class="row justify-content-sm-center align-items-end mt-4 video-pair">
  <div class="col-md-6 mt-3 mt-md-0">
    {% include video.liquid path="assets/video/seaicemicrostructure.mp4" class="img-fluid" controls=true autoplay=true loop=true muted=true playsinline=true nodownload=true %}
    <div class="caption">Microstructural evolution of sea ice at the ice-ocean boundary during top-down freezing. Video shows the spatiotemporal evolution of brine salinity. Video credit: Junning Liu.</div>
  </div>
  <div class="col-md-6 mt-3 mt-md-0">
    {% include video.liquid path="assets/video/seaiceconvection.mp4" class="img-fluid" controls=true autoplay=true loop=true muted=true playsinline=true nodownload=true %}
    <div class="caption">Buoyancy-driven convective transport of brine during interfacial melting of sea ice. Video shows the spatiotemporal evolution of brine salinity. Video credit: Junning Liu. </div>
  </div>
</div>

---

## Dry snow metamorphism

Ice-sediment mixtures are commonly found in `terrestrial permafrost` and `extraterrestrial regolith`. Under dry conditions, spatiotemporal variations in temperature and vapor pressure cause the redistribution of ice within the pore spaces through three key `pore-scale` processes - `ice migration`, `coarsening`, and `aggregation`. These processes strongly influence the long-term stability of subsurface ice, yet their underlying mechanisms remain poorly understood. Here, we aim to develop a mechanistic understanding of these `pore-scale` processes using `phase-field` simulations of `ice sublimation` and `vapor deposition`. 

<div class="row justify-content-sm-center mt-4 video-pair">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include video.liquid path="assets/video/dsm.mp4" class="img-fluid" controls=true autoplay=true loop=true muted=true playsinline=true nodownload=true %}
    <div class="caption">Pore-scale simulation of vapor-driven ice migration and coarsening in a tortuous pore space. Video shows the spatiotemporal evolution of vapor density. Video credit: Jackson Baglino.</div>
  </div>
</div>

---

## Droplet-laden turbulent reacting flows

Turbulent reacting sprays are ubiquitous in gas turbines and internal combustion engines. The combustion performance of these systems is governed by complex multiphysics interactions involving `droplet clustering`, `droplet evaporation` and `turbulent gas-phase combustion`. Each of these multiphysics processes have been well understood independently, but their coupled interactions remain poorly understood. A fundamental understanding of these coupled multiphysics interactions is, however, important for designing combustion systems with enhanced energy efficiency and reduced pollutant emissions. Here, we perform `point-droplet` three-dimensional `direct numerical simulations` of `droplet-laden reactive turbulence` to better understand the mechanisms governing these coupled multiphysics interactions and to classify the local combustion regimes under different flow conditions. 

<div class="row justify-content-sm-center mt-4 video-pair">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include video.liquid path="assets/video/turb-comb.mp4" class="img-fluid" controls=true autoplay=true loop=true muted=true playsinline=true nodownload=true %}
    <div class="caption">Two-dimensional slices of decane vapor mass fraction (left) and gas-phase temperature (right). Droplets are shown as black circles, and magnified for visualization purposes.</div>
  </div>
</div>

---

## References

<div class="publications reference-list">
  {% bibliography --query @*[key=bhopalam2026tbd1] --template bib_reference %}
  {% bibliography --query @*[key=bhopalam2026tbd3] --template bib_reference %}
  {% bibliography --query @*[key=weiss2021droplets] --template bib_reference %}
</div>
