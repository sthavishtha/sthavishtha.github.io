---
layout: page
title: Mechanics of fluid-structure interaction
description: Elasto-capillarity between immiscible fluids and nonlinear elastic solids
img: assets/img/publication_preview/fibrotaxis.png
importance: 3
category: research
_styles: >
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
  }
  .video-pair .caption {
    margin-top: 0.4rem;
    font-size: 0.85rem;
  }
---

## Bubble/droplet transport on soft solids

We have recently pioneered the concept of `droplet fibrotaxis`, a new droplet transport mechanism that enables droplet motion on `soft anisotropic solids`. The droplet transport herein, emerges from `elasto-capillary` interactions between the droplet and the underlying anisotropic solid. This droplet transport mechanism complements other elasto-capillary driven droplet transport mechanisms, such as [durotaxis](https://doi.org/10.1073/pnas.1307122110), [tensotaxis](https://doi.org/10.1016/j.eml.2017.01.004), [bendotaxis](https://doi.org/10.1103/PhysRevLett.122.074503) and substrate stretching. Droplet fibrotaxis has potential applications in self-cleaning surfaces, microfluidics, lab-on-a-chip technologies, and medical diagnostics, where interactions between deformable solids and droplets play an important role.

<div class="row justify-content-sm-center align-items-center mt-4 video-pair">
  <div class="col-md-5 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/pages/fibroschematic.png" class="img-fluid" alt="Droplet resting on a fiber-reinforced soft solid, with the fiber orientation indicated" %}
    <div class="caption">A droplet on a soft solid reinforced by fibers along a preferred orientation.</div>
  </div>
  <div class="col-md-7 mt-3 mt-md-0">
    {% include video.liquid path="assets/video/Fibrotaxis_3D_planar.mp4" class="img-fluid" controls=true autoplay=true loop=true muted=true playsinline=true nodownload=true %}
    <div class="caption">Three-dimensional simulation of droplet fibrotaxis on a planar fiber-reinforced substrate.</div>
  </div>
</div>

---

## Bubble/droplet transport in confined soft geometries