---
layout: page
title: Static and Dynamic Characterization of Flash ADC
description: CHIPS Design Studio - 2026
img: assets/img/projects/thesis/frankie-thesis-thumbnail.png
importance: 1
category: Research
related_publications: true
---

[Download Full Thesis (PDF)]({{ '/assets/projects/thesis/FRANKIE_THESIS_FINAL_DRAFT.pdf' | relative_url }})

[Download Thesis Presentation (PDF)]({{ '/assets/projects/thesis/Frankie Marrocco Thesis Presentation.pdf' | relative_url | replace: ' ', '%20' }})

# Abstract 

The  rapid  scaling  of  global  semiconductor  manufacturing  has  made  de-
vice characterization an essential pillar of modern supply chains.  Among the
most ubiquitous mixed-signal building blocks, the analog-to-digital converter
(ADC) demands rigorous performance  validation to ensure  the reliability  of
the systems that use them.

This thesis presents the design, implementation, and characterization of
a 4 MS/s 8-bit Flash ADC fabricated in 180 nm CMOS process for use as a
readout converter in a CMOS image sensor.  Two identical ADC instances are
implemented to serve even and odd pixel columns respectively, providing the
imager with a frame rate of approximately 40 FPS. The architecture follows
the standard Flash topology:  a sample and hold circuit with a slew rate of
about 3.6V/μs, a comparator with a pre-charged PMOS and latch structure,
and typical one-hot ROM encoder.

Device characterization strictly follows the IEEE 1241 standard for ADC
testing,  utilizing  standard  laboratory  equipment,  Verilog  control  logic  on  a
custom PCB, and a Python GUI for automatic data acquisition and process-
ing.  Measured static performance yielded a peak DNL of +3.15/-1.0 LSB and
INL of +2.68 / -3.19 LSB. Dynamic characterization at 4 MS/s produced an
SINAD of 31.52 dB, THD of -32.9 dBFS, and an ENOB of 4.94 bits.  Beyond
ADC  characterization,  this  work  establishes  a  reusable  test  framework  and
documented procedure to support future integrated circuit validation efforts.


# Test Setup

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/projects/thesis/test_setup_real_life_labled.jpg" title="Test setup" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/projects/thesis/test_setup.jpg" title="Test setup" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
