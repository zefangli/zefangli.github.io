---
title: "Gallery"
permalink: /gallery/
layout: single
author_profile: true
classes: wide
gallery:
  - url: https://doi.org/10.1080/17452759.2026.2694273
    image_path: /assets/imgs/gallery/6_rpp.jpg
    alt: "Concurrent two-nozzle printing of a multimaterial lattice"
    label: "Multimaterial print path planning · _Virtual Phys. Prototyp._ 2026"
    caption: |
      **What:** A planner for printing multimaterial lattices with several fixed-offset nozzles printing at the same time.
      **How:** I cast toolpath planning as a Rural Postman Problem on the lattice graph shifted by each nozzle's offset, then solved it with matching and an Eulerian circuit and exported G-code.
      **Why:** Graph routing gives near-optimal continuous paths with few non-printing jumps, cutting print time by up to 18%.
  - url: https://www.sciencedirect.com/science/article/pii/S1526612526005281
    image_path: /assets/imgs/gallery/5_meam.png
    alt: "Aluminum bunny printed by metal extrusion additive manufacturing"
    label: "Metal extrusion AM of aluminum · _J. Manuf. Processes_ 2026"
    caption: |
      **What:** Stable metal extrusion printing of thin-walled aluminum-alloy parts.
      **How:** I used thermal modeling of the part during printing to set the process parameters.
      **Why:** Thin walls trap heat and slump. Choosing parameters from thermal information replaces trial and error.
  - url: https://www.cell.com/matter/abstract/S2590-2385(25)00463-1
    image_path: /assets/imgs/gallery/4_lm.png
    alt: "3D-printed liquid metal foam structure"
    label: "Liquid metal foam emulsions · _Matter_ 2025"
    caption: |
      **What:** A 3D-printable liquid metal foam.
      **How:** I emulsified oil into liquid metal to make a paste-like ink for direct ink writing.
      **Why:** Bare liquid metal beads up and won't hold a shape. The emulsion makes it printable into free-standing structures.
  - url: https://advanced.onlinelibrary.wiley.com/doi/abs/10.1002/admt.202500422
    image_path: /assets/imgs/gallery/3_ultrawide.png
    alt: "3D-printed thiol-ene photopolymer bird"
    label: "Ultrawide-range photopolymers · _Adv. Mater. Technol._ 2025"
    caption: |
      **What:** A thiol-ene resin family whose stiffness spans five orders of magnitude and two full Shore hardness scales.
      **How:** I paired two extreme formulations with very different cross-link densities but the same curing chemistry. They can be blended for intermediate properties or mixed in situ for continuous gradients.
      **Why:** A shared curing mechanism keeps every blend printable, so one print can go from soft to rigid without manual assembly.
  - url: https://www.nature.com/articles/s41467-025-62313-9
    image_path: /assets/imgs/gallery/2_lce.jpg
    alt: "Radiofrequency-actuated liquid crystal elastomer turtle"
    label: "Radio-frequency LCE actuation · _Nat. Commun._ 2025"
    caption: |
      **What:** Wireless, frequency-selective actuation of soft robots with 2.4 GHz radio waves, even around obstacles.
      **How:** I made liquid crystal elastomer (LCE) actuators with a low actuation temperature, embedded with traces that resonate and heat at chosen frequencies. A beamforming platform steers power to them.
      **Why:** Tuning each actuator to its own frequency lets one transmitter drive them independently, without batteries, wires, or line of sight.
  - url: https://onlinelibrary.wiley.com/doi/10.1002/aisy.202200402
    image_path: /assets/imgs/gallery/1_lce.jpg
    alt: "Wrinkled liquid crystal elastomer surface"
    label: "Dynamic LCE wrinkling · _Adv. Intell. Syst._ 2024"
    caption: |
      **What:** Electrically controlled surface wrinkles of 17–45 μm, formed within 30 s at about 1 V.
      **How:** I built an LCE–elastomer bilayer with embedded liquid-metal ink. Joule heating actuates the LCE and wrinkles the bilayer.
      **Why:** Low-voltage electrical heating can be controlled locally, and the all-soft build lets cells tile into arrays that conform to curved surfaces.
  - url: https://doi.org/10.1016/j.mechrescom.2021.103695
    image_path: /assets/imgs/gallery/0_ring.jpg
    alt: "Model of a rotating bi-material ring"
    label: "Rotating bi-material ring · _Mech. Res. Commun._ 2021"
    caption: |
      **What:** A closed-form elastic solution for a rotating bi-material ring cooled below its manufacturing temperature.
      **How:** Superposition of a particular solution for rotation and a stress-function solution for the thermal mismatch, checked against numerical results.
      **Why:** A closed form gives stresses instantly and shows how geometry and materials drive them.
---

<style>
.paper-gallery { display: grid; grid-template-columns: repeat(auto-fill, minmax(240px, 1fr)); gap: 1.5em; }
.paper-gallery figure { margin: 0; display: block; }
.paper-gallery img { width: 100%; aspect-ratio: 1; object-fit: cover; }
.paper-gallery figcaption { margin: 0.5em 0 0; }
.paper-gallery figcaption p { margin: 0.3em 0 0; }
</style>

Images from my journal papers, newest first. Click an image to open the paper.

<div class="paper-gallery">
{% for img in page.gallery %}
<figure>
<a href="{{ img.url }}"><img src="{{ img.image_path | relative_url }}" alt="{{ img.alt | escape_once }}"></a>
<figcaption>
<a href="{{ img.url }}"><strong>{{ img.label | markdownify | remove: "<p>" | remove: "</p>" | strip }}</strong></a>
{{ img.caption | strip | newline_to_br | markdownify }}
</figcaption>
</figure>
{% endfor %}
</div>
