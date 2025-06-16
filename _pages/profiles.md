---
layout: page
permalink: /people/
title: People
description: Members of Our Group
nav: true
nav_order: 2

groups:
  - name: "Collaborating Faculty"
    profiles:
      - name: "Liang Zhao" 
        image: LiangZhao.jpg
        image_circular: true
        url: "https://www.research.ed.ac.uk/en/persons/liang-zhao"
  - name: "Postdoc"
    profiles:
      - name: "Tiancheng Li"
        image: TianchengLi.jpg
        image_circular: true
        url: "https://tianchengli-robotics.github.io/"
  - name: "PhD Students"
    profiles:
      - name: "Yingyu Wang"
        image: YingyuWang.png
        image_circular: true
        url: "https://wangyingyu.github.io"
      - name: "Yang Song"
        image: Yang_Song.jpg
        image_circular: true
        url: "https://yangsong-slam.github.io/"
      - name: "Kai Pan"
        image: KaiPan.jpg
        image_circular: true
        url: "https://drkaipan.github.io/"
      - name: "Dominik Slomma"
        image: Dominik.jpg
        image_circular: true
        url: "https://dominikslomma.github.io/"
      - name: "Yiran Zhou"
        image: YiranZhou.jpg
        image_circular: true
        url: "https://yiranzhou-robotics.github.io"
      - name: "Isira Damsith Wijegunawardana"
        image: Isira.jpg
        image_circular: true
        url: "https://sites.google.com/view/isiradwije"
      - name: "Chonghao Cheng"
        image: ChonghaoCheng.jpg
        image_circular: true
        url: 
      - name: "Zhihao Xing"
        image: ZhihaoXing.jpg
        image_circular: true
        url: " https://vglx.github.io/"
      - name: "Zhenzi Li"
        image: ZhenziLi.jpg
        image_circular: true
  - name: "Master Student"
    profiles:
      - name: "Duc"
        image: Duc.jpeg
        image_circular: true
        url: "https://www.linkedin.com/me?trk=p_mwlite_feed-secondary_nav"
  - name: "Visiting"
    profiles:
      - name: "Ranxi Liu"
        image: RanxiLiu.png
        image_circular: true
        url: "https://ranxiliu-uts.github.io"
  - name: "Alumni"
    profiles:
      - name: "Mengya Xu"
        image: MengyaXu.jpg
        image_circular: true
        url: "https://mengyaxu.github.io"
      - name: "Shengduo Chen"
        image: ShengduoChen.png
        image_circular: true
        url: "https://chenshengduo.github.io/"
      - name: "Yanhao Zhang"
        image: YanhaoZhang.jpg
        image_circular: true
        url: "https://sites.google.com/view/yanhaozhang/home"
      - name: "Yongbo Chen"
        image: YongboChen.jpg
        image_circular: true
        url: "https://sites.google.com/view/yongbochen"
      - name: "Jiaheng Zhao"
        image: prof_pic.jpg
        image_circular: true
        url: "https://jiahengzhao.github.io//publications/"
      - name: "Shuai Zhang"
        image: prof_pic.jpg
        image_circular: true
      - name: "Zhehua Mao"
        image: prof_pic.jpg
        image_circular: true
      - name: "Hongkyoon Byun"
        image: Hugh.jpg
        image_circular: true
        url: "https://www.linkedin.com/in/hughbyun/"
      - name: "Youbing Wang"
        image: YoubingWang.jpeg
        image_circular: true
        url: " https://www.linkedin.com/in/y-ben-wang-b0549193/"
      - name: "Jun Wang"
        image: JunWang.jpeg
        image_circular: true
        url: "https://scholar.google.com/citations?user=Ao2IF4QAAAAJ&hl=en"
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
