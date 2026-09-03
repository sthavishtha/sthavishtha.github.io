---
layout: page
title: Fluid-structure interaction
img: assets/img/publication_preview/fibrotaxis.png
importance: 3
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
  .video-pair video,
  .video-pair img {
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
    .video-pair img.schematic {
      width: auto;
      max-width: 100%;
      max-height: 200px;
      display: block;
      margin: 0 auto;
    }
  }
  .video-pair .caption {
    margin-top: 0.4rem;
    font-size: 0.85rem;
  }
---

<div class="theme-lead" markdown="1">
I have used `computational multiphase fluid-structure interaction` models to uncover new fundamental mechanisms involving `capillarity`, fluid flow and deformation of `soft materials` in `micro- and nano-scale systems`. At these length-scales, the deformation of `soft materials` is driven primarily by `capillary forces` acting at the fluid-fluid interfaces. My interest in this field is motivated by the limited availability of predictive computational frameworks for accurately modeling and understanding such interfacial phenomena.
</div>

## Spontaneous droplet transport on soft solids

Droplet transport is important in a wide range of applications, including `self-cleaning of surfaces`, `microfluidics`, `lab-on-a-chip technologies`, and `medical diagnostics`. Spontaneous droplet transport on rigid solids has been well established; however, the spontaneous motion of droplets on soft solids remains relatively less explored. Here, we propose `droplet fibrotaxis`, a new droplet transport mechanism that enables directional, spontaneous and gradient-free droplet motion on `soft anisotropic solids`. Droplet motion in `fibrotaxis` arises from [elasto-capillarity](https://doi.org/10.1146/annurev-conmatphys-031016-025326), and it complements other elasto-capillary driven droplet transport mechanisms, such as [durotaxis](https://doi.org/10.1073/pnas.1307122110), [tensotaxis](https://doi.org/10.1016/j.eml.2017.01.004), and [bendotaxis](https://doi.org/10.1103/PhysRevLett.122.074503). 

<div class="row justify-content-sm-center align-items-center mt-4 video-pair">
  <div class="col-md-5 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/pages/fibroschematic.png" class="img-fluid schematic" alt="Droplet resting on a fiber-reinforced soft solid, with the fiber orientation indicated" %}
    <div class="caption">Schematic of a droplet on a fiber-reinforced deformable solid. The white arrow depicts the orientation of fibers. Image credit: DALL-E </div>
  </div>
  <div class="col-md-7 mt-3 mt-md-0">
    {% include video.liquid path="assets/video/Fibrotaxis_3D_planar.mp4" class="img-fluid" controls=true autoplay=true loop=true muted=true playsinline=true nodownload=true %}
    <div class="caption">Video of a three-dimensional simulation demonstrating droplet fibrotaxis. The black arrow depicts the orientation of fibers. </div>
  </div>
</div>

---

## Bubble/droplet transport in confined soft geometries

Using direct numerical simulations of `two-fluid fluid-structure interactions` in capillary tubes, we have explored strategies to effectively control (a) the onset of `interfacial instabilities` and `droplet/bubble pinch-off`, and (b) the transport of droplets/bubbles through `constricted spaces`. Our high-resolution simulations show that (a) tube’s deformability can either suppress or delay the onset of `interfacial instabilities` and `pinch-off` relative to rigid tubes, and (b) `tube’s actuation` is an effective way to transport droplets/bubbles through constricted spaces. Our findings are important in many applications, such as `enhanced oil recovery`, `inkjet printing`, `microfluidics`, and `drug delivery systems`.

<div class="row justify-content-sm-center align-items-center mt-4 video-pair">
  <div class="col-md-5 mt-3 mt-md-0">
    {% include video.liquid path="assets/video/forcing_actuation.mp4" class="img-fluid" controls=true autoplay=true loop=true muted=true playsinline=true nodownload=true %}
    <div class="caption">Simulation of an oil droplet (shown in white) transported through an actuated, constricted deformable capillary tube (shown in brown) filled with water.
    </div>
  </div>
  <div class="col-md-7 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/video/bpinchoff.gif" class="img-fluid schematic" avoid_scaling=true alt="Bubble confined inside a deformable capillary tube" %}
    <div class="caption">Simulation of an air bubble (shown in white) pinched off in a deformable capillary tube (shown in brown) filled with glycerol. </div>
  </div>
</div>

---

## References

<div class="publications reference-list">
  {% bibliography --query @*[key=bhopalam2026droplet] --template bib_reference %}
  {% bibliography --query @*[key=bhopalam2026simulating] --template bib_reference %}
  {% bibliography --query @*[key=bhopalam2024fibrotaxis] --template bib_reference %}
</div>
