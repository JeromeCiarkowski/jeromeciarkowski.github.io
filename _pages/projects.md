---
permalink: /projects/
layout: category
taxonomy: null
author_profile: true
title: Projects
project5:
  - image_path: assets/images/coming-soon.gif
    title: Halo iOS Theme
    excerpt: TODO
    url: jeromeciarkowski.github.io/blog/halo-ios-theme
    btn_label: READ
    btn_class: btn--primary
project4:
  - image_path: assets/images/coming-soon.gif
    title: Twitch Account
    excerpt: TODO
    url: jeromeciarkowski.github.io/blog/twitch-account
    btn_label: READ
    btn_class: btn--primary
project3:
  - image_path: assets/images/coming-soon.gif
    title: Doom Eternal | Orthogonal Unit Differentiation Chart
    excerpt: TODO
    url: jeromeciarkowski.github.io/blog/doom-eternal-othogonal-unit-differentiation-chart
    btn_label: READ
    btn_class: btn--primary
project2:
  - image_path: assets/images/coming-soon.gif
    title: Uplift Desk Assembly | Stop Motion Video
    excerpt: TODO
    url: jeromeciarkowski.github.io/blog/uplift-desk-assembly-stop-motion-video
    btn_label: READ
    btn_class: btn--primary
project1:
  - image_path: assets/images/coming-soon.gif
    title: WordPress Personal Website
    excerpt: TODO
    url: jeromeciarkowski.github.io/blog/wordpress-personal-website
    btn_label: READ
    btn_class: btn--primary
---

{% if paginator %}
  {% assign posts = paginator.posts %}
{% else %}
  {% assign posts = site.posts %}
{% endif %}

{% assign index = 0 %}

{% for post in posts %}
  {% assign mod = forloop.index | modulo: 2 %}
  {% assign project_index = "project" | append: forloop.index %}
  {% if mod == 1 %}
    {% include feature_row id=project_index type="left" %}
  {% endif %}
  {% if mod == 0 %}
    {% include feature_row id=project_index type="right" %}
  {% endif %}
{% endfor %}