---
layout: page
permalink: /people/
title: People
description: Members of our group
nav: true
nav_order: 1

groups:
  - name: "Postdoc"
    profiles:
  - name: "PhD Students"
    profiles:
      - name: "Yingyu Wang"
        image: YingyuWang.png
        image_circular: true
        url: "https://wangyingyu.github.io"
      - name: "Yang Song"
        image: prof_pic.jpg
        image_circular: true
      - name: "Tiancheng Li"
        image: prof_pic.jpg
        image_circular: true
      - name: "Kai Pan"
        image: prof_pic.jpg
        image_circular: true
      - name: "Dominik Slomma"
        image: prof_pic.jpg
        image_circular: true
      - name: "Yiran Zhou"
        image: YiranZhou.jpg
        image_circular: true
      - name: "Isira Damsith Wijegunawardana"
        image: prof_pic.jpg
        image_circular: true
      - name: "Chonghao Chen"
        image: prof_pic.jpg
        image_circular: true
      - name: "Zhihao Xing"
        image: prof_pic.jpg
        image_circular: true
      - name: "Zhenzi Li"
        image: ZhenziLi.jpg
        image_circular: true
  - name: "Master Student"
    profiles:
      - name: "Duc"
        image: prof_pic.jpg
        image_circular: true
        url: "https://wangyingyu.github.io"
  - name: "Visiting"
    profiles:
      - name: "Ranxi Liu"
        image: prof_pic.jpg
        image_circular: true
  - name: "Alumni"
    profiles:
      - name: "Mengya Xu"
        image: MengyaXu.jpg
        image_circular: true
---

{% for group in page.groups %}

<section class="group-section">
  <h2>{{ group.name }}</h2>
  <div class="row">
    {% for profile in group.profiles %}
      <div class="col-md-3 col-sm-6 text-center profile-item" style="margin-bottom: 30px;">
        {% if profile.image %}
          {% assign profile_image_path = profile.image | prepend: 'assets/img/' %}
          {% if profile.image_circular %}
            {% assign profile_image_class = 'img-fluid img-circular' %}
          {% else %}
            {% assign profile_image_class = 'img-fluid rounded' %}
          {% endif %}
          {% capture sizes %}(min-width: {{ site.max_width }}) {{ site.max_width | minus: 30 | times: 0.3 }}px, (min-width: 576px) 30vw, 95vw{% endcapture %}
          {% if profile.url %}
            <a href="{{ profile.url }}" target="_blank">
              {% include figure.liquid loading="eager" path=profile_image_path class=profile_image_class sizes=sizes alt=profile.name %}
            </a>
          {% else %}
            {% include figure.liquid loading="eager" path=profile_image_path class=profile_image_class sizes=sizes alt=profile.name %}
          {% endif %}
        {% endif %}
        {% if profile.name %}
          {% if profile.url %}
            <h3 class="profile-name"><a href="{{ profile.url }}" target="_blank">{{ profile.name }}</a></h3>
          {% else %}
            <h3 class="profile-name">{{ profile.name }}</h3>
          {% endif %}
        {% endif %}
      </div>
    {% endfor %}
  </div>
</section>
{% endfor %}
