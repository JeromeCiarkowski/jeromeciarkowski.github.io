---
permalink: /
layout: splash
header:
  overlay_image: /assets/images/machu-picchu.jpeg
  caption: "TODO: Visit Machu Picchu, Snap Photo, Change Banner"
  actions:
    - label: LET'S A-GO!
      url: https://jeromeciarkowski.github.io/blog
excerpt: /jer-rome chur-kow-skee/ <br>(noun) <br>1. An enthusiast of choice architecture, software engineering, video games, bodybuilding, and distractions from the game of life
intro: 
  - excerpt: "Hello, friend! Welcome to my personal website:<br>a curated digital medium where I detail my experiments, projects, and insights about any which topic that piques my curiosity. Typically, my attention is focused toward choice architecture, software engineering, video games, and bodybuilding--but I venture into the unknown from time to time. Hopefully, my words will showcase my depth as a person, a potential employee, and remain as a relic of history on the Internet."
feature_row:
  - image_path: assets/images/bio-photo.jpg
    title: "Blog"
    excerpt: Short-form literature
    url: localhost:4000/blog
    btn_label: READ
    btn_class: btn btn--light-outline
  - image_path: /assets/images/pc-digital-chameleon.jpeg
    title: Projects
    excerpt: Long-form literature
    url: localhost:4000/projects  
    btn_label: DISCOVER
    btn_class: btn btn--light-outline
  - image_path: /assets/images/jerome-suit.jpeg
    title: Resume
    excerpt: TODO
    url: localhost:4000/resume
    btn_label: INTERVIEW
    btn_class: btn btn--light-outline
entries_layout: grid
---

{% include feature_row id="intro" type="center" %}

{% include feature_row %}

{% if paginator %}
  {% assign posts = paginator.posts %}
{% else %}
  {% assign posts = site.posts %}
{% endif %}

{% for post in posts %}
  {% include archive-single.html %}
{% endfor %}