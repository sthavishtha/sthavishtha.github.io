---
layout: page
title: Fluid-structure interaction
img: assets/img/publication_preview/fibrotaxis.png
importance: 3
category: research
_styles: >
  .theme-lead {
    margin: 0 0 2.25rem;
    padding: 1.15rem 1.5rem;
    border-left: 3px solid var(--global-theme-color);
    border-radius: 0 8px 8px 0;
    background-color: var(--global-code-bg-color);
    background-color: color-mix(in srgb, var(--global-theme-color) 6%, transparent);
    font-size: 1.05rem;
    line-height: 1.65;
  }
  .theme-lead p:last-child {
    margin-bottom: 0;
  }
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
I have used `computational multiphase fluid-structure interaction` models to uncover new fundamental mechanisms involving `capillarity`, fluid flow and solid deformation of `soft materials` in `micro- and nano-scale systems`. At these length-scales, the deformation of `soft materials` is driven primarily by `capillary forces`. My interest in this field is motivated by the limited availability of predictive computational frameworks for accurately modeling and understanding such interfacial phenomena.
</div>

## Bubble/droplet transport on soft solids

We have recently pioneered the concept of `droplet fibrotaxis`, a new droplet transport mechanism that enables spontaneous droplet motion on `soft anisotropic solids`. The droplet transport herein, emerges from [elasto-capillary](https://doi.org/10.1146/annurev-conmatphys-031016-025326) interactions between the droplet and the underlying anisotropic solid. This droplet transport mechanism complements other elasto-capillary driven droplet transport mechanisms, such as [durotaxis](https://doi.org/10.1073/pnas.1307122110), [tensotaxis](https://doi.org/10.1016/j.eml.2017.01.004), [bendotaxis](https://doi.org/10.1103/PhysRevLett.122.074503) and substrate stretching. Droplet fibrotaxis has potential applications in `self-cleaning of surfaces, microfluidics, lab-on-a-chip technologies, and medical diagnostics`, where interactions between deformable solids and droplets play an important role.

<div class="row justify-content-sm-center align-items-center mt-4 video-pair">
  <div class="col-md-5 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/pages/fibroschematic.png" class="img-fluid schematic" alt="Droplet resting on a fiber-reinforced soft solid, with the fiber orientation indicated" %}
    <div class="caption">Schematic of a droplet on a fiber-reinforced deformable solid with embedded fibers inducing anisotropy.</div>
  </div>
  <div class="col-md-7 mt-3 mt-md-0">
    {% include video.liquid path="assets/video/Fibrotaxis_3D_planar.mp4" class="img-fluid" controls=true autoplay=true loop=true muted=true playsinline=true nodownload=true %}
    <div class="caption">Three-dimensional simulation of droplet fibrotaxis.</div>
  </div>
</div>

---

## Bubble/droplet transport in confined soft geometries

Using direct numerical simulations of `two-fluid fluid-structure interactions` in capillary tubes, we have explored strategies to effectively control (a) the onset of `interfacial instabilities` and `droplet/bubble pinch-off`, and (b) the transport of droplets/bubbles through `constricted spaces`. Our high-resolution simulations show that (a) tube’s deformability can either suppress or delay the onset of `interfacial instabilities` and `pinch-off` relative to rigid tubes, and (b) `tube’s actuation` is an effective way to transport droplets/bubbles through constricted spaces. Our findings are important in many applications, such as `enhanced oil recovery, inkjet printing, microfluidics, drug delivery systems, plant biological systems, and manufacturing`.

<div class="row justify-content-sm-center align-items-center mt-4 video-pair">
  <div class="col-md-4 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/video/bpinchoff.gif" class="img-fluid schematic" avoid_scaling=true alt="Bubble confined inside a deformable capillary tube" %}
    <div class="caption">Schematic of a bubble confined in a deformable capillary tube.</div>
  </div>
  <div class="col-md-8 mt-3 mt-md-0">
    {% include video.liquid path="assets/video/forcing_actuation.mp4" class="img-fluid" controls=true autoplay=true loop=true muted=true playsinline=true nodownload=true %}
    <div class="caption">Simulation of bubble transport through a constricted deformable tube driven by tube actuation.</div>
  </div>
</div>

---

## References

<div class="publications reference-list">
  {% bibliography --query @*[key=bhopalam2026droplet] --template bib_reference %}
  {% bibliography --query @*[key=bhopalam2026simulating] --template bib_reference %}
  {% bibliography --query @*[key=bhopalam2024fibrotaxis] --template bib_reference %}
</div>
