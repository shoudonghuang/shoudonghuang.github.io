---
layout: page
permalink: /people/
title: People
description: Members of our group
nav: true
nav_order: 1

groups:
  - name: "Current Student"
    profiles:
      - name: "Yingyu Wang"
        image: prof_pic.jpg
        image_circular: false
      - name: "Tiancheng Li"
        image: prof_pic.jpg
        image_circular: false
      - name: "Yang Song"
        image: prof_pic.jpg
        image_circular: false
  - name: "Alumni"
    profiles:
      - name: "David"
        image: prof_pic.jpg
        image_circular: false
      - name: "Eve"
        image: prof_pic.jpg
        image_circular: false
      - name: "Frank"
        image: prof_pic.jpg
        image_circular: false
---

{% for group in page.groups %}

<section class="group-section">
  <h2>{{ group.name }}</h2>
  <div class="row">
    {% for profile in group.profiles %}
      <div class="col-md-4 col-sm-6 text-center profile-item" style="margin-bottom: 30px;">
        {% if profile.image %}
          {% assign profile_image_path = profile.image | prepend: 'assets/img/' %}
          {% if profile.image_circular %}
            {% assign profile_image_class = 'img-fluid rounded-circle' %}
          {% else %}
            {% assign profile_image_class = 'img-fluid rounded' %}
          {% endif %}
          {% capture sizes %}(min-width: {{ site.max_width }}) {{ site.max_width | minus: 30 | times: 0.3 }}px, (min-width: 576px) 30vw, 95vw{% endcapture %}
          {% include figure.liquid loading="eager" path=profile_image_path class=profile_image_class sizes=sizes alt=profile.name %}
        {% endif %}
        <h3 class="profile-name">{{ profile.name }}</h3>
      </div>
    {% endfor %}
  </div>
</section>
{% endfor %}
