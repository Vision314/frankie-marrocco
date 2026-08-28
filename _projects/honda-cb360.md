---
layout: page
date: 2026-08-01
title: Honda CB360
description: Repairs & Pictures
img: assets/img/projects/cb360/bike-pics/thumbnail.PNG
importance: 10
category: Other
related_publications: false
selected: false
toc:
  sidebar: left
---


On Monday, July 27th, I saw a Honda CB360 on Facebook Marketplace for $1,900. The day before I got a job offer and I knew I'd be moving to Boston soon, so I wanted to get myself a present for doing a good job. At 10:00 AM I messaged the seller and at 1:00 PM he dropped it off at my house.


{% assign carousel_files = site.static_files | where_exp: "f", "f.path contains 'assets/img/projects/cb360/bike-pics/'" %}
{% assign carousel_files = carousel_files | where_exp: "f", "f.basename != 'thumbnail'" %}
{% assign carousel_files = carousel_files | where_exp: "f", "f.extname != '.webp'" %}
{% assign carousel_files = carousel_files | sort: "basename" %}

{% if carousel_files.size > 0 %}
<div style="overflow-x: auto; padding-bottom: 0.5rem;">
  <div style="display: flex; gap: 1rem; width: max-content; margin: 0 auto;">
    {% for file in carousel_files %}
      {% assign ext = file.extname | downcase %}
      <div style="width: 220px;">
        {% if ext == '.mp4' or ext == '.webm' or ext == '.ogg' or ext == '.mov' %}
          <video
            src="{{ file.path | relative_url }}"
            class="img-fluid rounded z-depth-1"
            style="width: 100%; height: 220px; object-fit: cover; background: #000;"
            controls
          ></video>
        {% else %}
          <img
            src="{{ file.path | relative_url }}"
            class="img-fluid rounded z-depth-1"
            style="width: 100%; height: 220px; object-fit: cover;"
            alt="{{ file.basename }}"
          >
        {% endif %}
      </div>
    {% endfor %}
  </div>
</div>
{% endif %}

I enjoy learning about engines and I like having a back burner project to work on in my free time. I don't have any crazy goals except to give it some attention, ride it locally, and maybe make a couple hundred dollars off of it.

This page is a blog of my progress. Hope you enjoy!


# Fixing the Horn

<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0 text-center">
    <div id="horn-off-fig">
      {% include figure.liquid path="assets/img/projects/cb360/fixing-horn/horn_schematic-off.png" title="Horn wiring, switch off" class="img-fluid rounded z-depth-1" alt="Horn wiring schematic with switch off" %}
    </div>
    <div id="horn-on-fig" style="display: none;">
      {% include figure.liquid path="assets/img/projects/cb360/fixing-horn/horn_schematic-on.png" title="Horn wiring, switch on" class="img-fluid rounded z-depth-1" alt="Horn wiring schematic with switch on" %}
    </div>
    <button id="horn-toggle-btn" type="button" class="btn btn-outline-primary mt-3" onclick="toggleHornSchematic()">Switch On</button>
  </div>
</div>

<script>
  function toggleHornSchematic() {
    var offFig = document.getElementById('horn-off-fig');
    var onFig = document.getElementById('horn-on-fig');
    var btn = document.getElementById('horn-toggle-btn');
    var isOff = offFig.style.display !== 'none';
    offFig.style.display = isOff ? 'none' : '';
    onFig.style.display = isOff ? '' : 'none';
    btn.textContent = isOff ? 'Switch Off' : 'Switch On';
  }
</script>

# Breaking the Throttle and Front Break Assembly

# 
