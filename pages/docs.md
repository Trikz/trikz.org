---
title: Documentation
permalink: /docs/
layout: page
---

# Documentation

Welcome to the {{ site.title }} Documentation pages! Here you can quickly jump to a 
particular page.

<div class="section-index">
    <hr class="panel-line">
    {% for post in site.docs  %}        
    <div class="entry">
    <h4><a href="{{ post.url }}">{{ post.title }}</a></h4>
    <p>{{ post.description }}</p>
    </div>{% endfor %}
</div>
