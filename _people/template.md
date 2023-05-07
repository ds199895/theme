---
name: Inst. AAA
title: Inst. AAA
image: https://avatars.githubusercontent.com/u/65162754?s=400&u=475e4bbd604bd5c95fc418b1dc6c7eacb00ca4df&v=4
navs: [template]
tags: [Ph.D. Student, 2019]
position: student
---
{% include elements/landing.html h1="Inst. AAA" h2="Institute of Architectural Algorithms & Applications<br>School of Architecture<br>Southeast University" image='https://avatars.githubusercontent.com/u/65162754?s=400&u=475e4bbd604bd5c95fc418b1dc6c7eacb00ca4df&v=4' %}


# **About Me**

Hi I am **{{ site.author.name }}** :wave:,<br>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.

<div class="row">
{% include elements/skills.html title="Programming Skills" source=site.data.programming-skills %}
{% include elements/skills.html title="Other Skills" source=site.data.other-skills %}
</div>

<div class="row">
{% include elements/timeline.html %}
</div>
{% assign carousel_items = "" | split: ',' %}

{% for p in site.projects %}
  {%- if p.image  -%}  
    {% assign carousel_items = carousel_items | push: p %}
  {% endif %}
{% endfor %}
{% include elements/project-carousel.html %}
