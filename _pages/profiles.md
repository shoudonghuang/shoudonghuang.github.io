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
      - align: right
        image: prof_pic.jpg
        content: Current_Student.md
        image_circular: false
        more_info: >
          <p>555 your office number</p>
          <p>123 your address street</p>
          <p>Your City, State 12345</p>
  - name: "Alumni"
    profiles:
      - align: left
        image: prof_pic.jpg
        content: Alumni.md
        image_circular: false
        more_info: >
          <p>555 your office number</p>
          <p>123 your address street</p>
          <p>Your City, State 12345</p>
---

{% for group in page.groups %}

<section class="group-section">
  <h2>{{ group.name }}</h2>
  {% for profile in group.profiles %}
    <div class="profile float-{% if profile.align == 'left' %}left{% else %}right{% endif %}">
      {% if profile.image %}
        {% assign profile_image_path = profile.image | prepend: 'assets/img/' %}
        {% if profile.image_circular %}
          {% assign profile_image_class = 'img-fluid rounded-circle' %}
        {% else %}
          {% assign profile_image_class = 'img-fluid rounded' %}
        {% endif %}
        {% capture sizes %}(min-width: {{ site.max_width }}) {{ site.max_width | minus: 30 | times: 0.3 }}px, (min-width: 576px) 30vw, 95vw{% endcapture %}
        {% include figure.liquid loading="eager" path=profile_image_path class=profile_image_class sizes=sizes alt=profile.image %}
      {% endif %}
      {% if profile.more_info %}
        <div class="more-info">{{ profile.more_info }}</div>
      {% endif %}
      {% if profile.content %}
        {% capture profile_content %}{% include_relative {{ profile.content }} %}{% endcapture %}
        {{ profile_content | markdownify }}
      {% endif %}
    </div>
    <div class="clearfix"></div>
  {% endfor %}
</section>
{% endfor %}
