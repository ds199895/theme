---
name: Yichen Mo
title: Yichen Mo
image: https://amomorning.github.io/assets/img/prof_pic-1400.webp
position: student
tags: [Ph.D. Student, 2019]
---

{% include elements/landing.html h1="Yichen Mo" h2='<a class="github-button" href="https://github.com/amomorning"
  data-size="large" data-show-count="true" aria-label="Follow @amomorning on GitHub">Follow @amomorning</a>'
image="https://amomorning.github.io/assets/img/prof_pic-1400.webp" %}

Yichen Mo is currently a PhD student at Southeast University advised by [Prof. Biao Li](/people/libiao). She started the Joint Doctoral
Program at the chair of [Digital Architectonics](https://www.caad.arch.ethz.ch) as a visiting student in 2022. Her research focuses on architectural representation learning and
geometry processing. She creates a web-based 3D editor [ArchiWeb](https://web.archialgo.com/#/) and corresponding protocol [ArchiJSON](https://www.food4rhino.com/en/app/archijson) for designing
algorithms and data structures for computational architecture. Yichen studied architecture and computer science at
Zhejiang Sci-Tech University and graduated with double degrees. She received DigitalFUTURES YOUNG STAR (2019) and <i class="fab fa-github" data-toggle="tooltip" data-placement="bottom" data-delay="250" title="GitHub Repository"></i> [Google
Girl Hackathon Season V Battle Winner](https://github.com/amomorning/google-girl-hackathon-v) in Shanghai.

<h4 class='text-center my-5'>Projects</h4>

{% assign carousel_items = site.projects | where:"team", "Yichen Mo" %}
{% assign carousel_items = carousel_items | where_exp:"item", "item.image"%}
{% include elements/project-carousel.html %}

<h4 class='text-center my-5'>Publications</h4>

<div class="row">
  {% assign publications = site.publications | where:"authors","Yichen Mo" %}

  {% for p in publications reversed%}

    <div class="col-2 py-2">
      {{p.date | date: "%Y/%m"}}
    </div>
    {% if forloop.first %}
    <div class="col-10 py-2">
    {% else %}

    <div class="col-10 py-2" style="border-top:1px solid">
    {% endif %}
      {{p.title}}, <i>{{p.subtitle}}</i>, {{p.date | date: "%Y"}}
      <br>
      <div class="text-muted">
        {{p.authors | join: ', '}}
      </div>

    </div>

  {% endfor%}
</div>

<br>
<br>
<br>
