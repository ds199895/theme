---
name:  He Siyuan
image: https://archialgo-com-sources.oss-cn-hangzhou.aliyuncs.com/images/hesiyuan2.jpg
tags: [Master Student, 2021]
position: student
---
{% include elements/landing.html h1="He Siyuan" h2="lalala" image='https://archialgo-com-sources.oss-cn-hangzhou.aliyuncs.com/images/hesiyuan2.jpg' %}

# 贺思远 HE Siyuan  
HE Siyuan is currently a Master student at Inst. AAA, Southeast University supervised by [Prof.  LI Biao](/people/libiao).  
东南大学建筑学院建筑运算与应用研究所（Inst. AAA）在读研究生，导师[李飚](/people/libiao)教授。  
本科期间就读于东南大学建筑学院。

<h4 class='text-center mt-5'>Projects</h4>

---

{% assign projects = site.projects | where:"team", "He Siyuan" %}
  {% for p in projects reversed %} 
    {%- if p.external_url -%}
    {%- assign project_url = p.external_url -%}
    {%- else -%}
    {%- assign project_url = p.url | relative_url -%}
    {%- endif -%}

    <div class="wow animated fadeIn col-4 p-2" data-wow-delay=".15s">
        <a href="{{ project_url }}" class="card border-dark rounded" {%- if external and site.open_new_tab -%} target="_blank" {%- endif -%}>
            {%- if p.image -%}
            <img id="{{ p.name }}-img" class="card-img-top m-0" src="{{ p.image }}" alt="{{ p.name }}" />
            {%- endif -%}

            <div class="card-body">
                <h6 id="{{ p.name }}-name" class="card-title text-themed">
                    {%- if project_type == "remote" -%}
                    <i class="fab fa-github" data-toggle="tooltip" data-placement="bottom" data-delay="250" title="GitHub Repository"></i> |&nbsp;
                    {%- endif -%}
                    {{ p.name }}
                </h6>
                <p id="{{ p.name }}-year" class="card-text mb-2 text-muted small">
                    {{ p.year }}

                    {% if p.location != empty %}
                    {{ p.location }}
                    {% endif %}
                </p>
            </div>
        </a>
    </div>

  {% endfor %}


<h4 class='text-center mt-5'>Publications</h4>

---

<div class="row">
  {% assign publications = site.publications | where:"authors","He Siyuan" %}

  {% for p in publications reversed%}
    {%- if p.external_url -%}
    {%- assign publication_url = p.external_url -%}
    {%- else -%}
    {%- assign publication_url = p.url | relative_url -%}
    {%- endif -%}

    
    <a href="{{ publication_url }}" class="my-0 col-12 p-0" {%- if p.external_url and site.open_new_tab -%} target="_blank" {%- endif -%}>
        <div class="card-body">
            <h5 class="card-title text-themed">{{ p.title }}</h5>
            <h6 class="card-subtitle mb-2 text-muted max-lines">{{ p.subtitle }}</h6>

            <h6 class="card-text small" style="color:gray">
                {{ p.authors | join: ", " }}
            </h6>

            <p class="card-text small">
                {{ p.date | date_to_long_string }} | {{ p.paper_type }}
            </p>
        </div> 
    </a>
    

  {% endfor %}
</div>

{% include elements/button-top.html %}