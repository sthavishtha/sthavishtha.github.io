---
layout: page
title: Computational mechanics
img: assets/img/publication_preview/iga.jpeg
importance: 1
category: research
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
---

<div class="theme-lead" markdown="1">
I have developed predictive models and computational methods for `moving contact line` problems in `fluid-structure interactions`, `multiphase flows`, and `porous media`.
</div>

## Fluid-structure interaction

Traditional computational methods for solving `fluid-structure interaction` (FSI) problems involving `multiphase fluids` have extensively focused on large-scale systems, where `capillary forces` at fluid-fluid interfaces have a negligible impact on solid deformation. However, at `micro- and nano-scales`, `capillary forces` acting at the fluid-fluid interfaces can signficantly `deform soft solids` and fundamentally alter fluid transport. To capture the multiphysics effects at such small length-scales, we have developed computational models and methods for `FSI` involving `multiphase fluids` in `confined soft geometries` and on `soft solids`. We use a `phase-field` description of fluids coupled with `nonlinear solid models` that can handle large deformations. Our models handle more than `two immiscible fluids`, `high flow rates`, and `advanced soft materials`, representing multiphysics regimes that have received less attention in the literature. 

<div class="row justify-content-sm-center align-items-end mt-4 video-pair">
  <div class="col-md-6 mt-3 mt-md-0">
    {% include video.liquid path="assets/video/janusdroplet_2.mp4" class="img-fluid" controls=true autoplay=true loop=true muted=true playsinline=true nodownload=true %}
  </div>
  <div class="col-md-6 mt-3 mt-md-0">
    {% include video.liquid path="assets/video/collardroplet_2.mp4" class="img-fluid" controls=true autoplay=true loop=true muted=true playsinline=true nodownload=true %}
  </div>
  <div class="caption">Simulation of capillary origami of Janus compound droplet (left) and collar compound droplet (right). Blue, red and gray colors denote water, oil and the deformable solid, respectively.</div>
</div>

## Multiphase flows

I have developed `computational multiphase flow` models to study two different categories of interfacial phenomena: `solidification` (liquid-solid phase transformations) and `particle-laden suspensions` (no phase transformations). For the first category, I have developed phase-field models for `droplet freezing` on ice that capture key wetting phenomena which remain poorly understood - `droplet spreading`, `partial wetting`, and `contact line pinning`. These models provide new fundamental insights into the dynamics of `unsaturated` flows in `ice-bearing porous media` systems under subfreezing conditions. For the second category, I have developed continuum models for simulating the displacement of `particle-laden suspensions` in `unsaturated Hele-Shaw cells`. These models mechanistically capture `shear-induced particle migration` and elucidate its role in the evolution of `particle-induced viscous fingering`. These continuum models can be used to better understand contaminant transport in soils, wastewater infiltration, and the transport of industrial slurries in confined systems. 

<div class="row justify-content-sm-center align-items-end mt-4 video-pair">
  <div class="col-md-6 mt-3 mt-md-0">
    {% include video.liquid path="assets/video/solidification.mp4" class="img-fluid" controls=true autoplay=true loop=true muted=true playsinline=true nodownload=true %}
    <div class="caption">Simulation video of droplet freezing on ice under subfreezing conditions.</div>
  </div>
  <div class="col-md-6 mt-3 mt-md-0">
    <div class="caption">Simulation video will be made available shortly. </div>
  </div>
</div>

## Porous media

Several continuum models have been developed to study the multiphysics behavior of `immiscible fluid flow` in `unsaturated poroelastic` media. These models typically neglect `capillary forces` and are primarily formulated for large length-scale problems. At small length-scales, however, `capillary forces` become important as they deform the porous skeleton and strongly influence the coupled fluid-solid response. To better understand the dynamics of two `immiscible fluids` in `unsaturated poroelastic` media at small length-scales, we have derived and developed `phase-field` models from first principles of continuum mechanics. Using these models, we have elucidated the mechanisms by which `capillary forces` influence the mechanical response of `unsaturated poroelastic` media. The key findings from our models can be used to better understand fluid transport in biological tissues and the deformation of soft porous materials.  

<div class="row justify-content-sm-center mt-4 video-pair">
  <div class="col-sm-10 mt-3 mt-md-0">
    <div class="caption">Simulation video will be made available shortly. </div>
  </div>
</div>

## References

<div class="publications reference-list">
  {% bibliography --query @*[key=bhopalam2022elastocapillary] --template bib_reference %}
  {% bibliography --query @*[key=bhopalam2026simulating] --template bib_reference %}
  {% bibliography --query @*[key=bhopalam2026tbd2] --template bib_reference %}
</div>
