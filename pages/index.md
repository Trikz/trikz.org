---
layout: landingpage
title: Trikz.org
permalink: /
---
<div id="header">
    {% capture site_title %}{% if page.title %}{{ page.title }}{% else %}{{ site.title }}{% endif %}{% endcapture %}
    {% capture site_description %}{% if page.description %}{{ page.description | newline_to_br }}{% else %}{{ site.description | newline_to_br }}{% endif %}{% endcapture %}
	<h1 class="title"><a href="/">{{ site_title }}</a></h1>
	<h2 class="description">{{ site_description }}</h2>
    <div class="buttonwrapper">
        <a class="md-source" data-md-source="github" href="{{ site.repo }}/projects" title="View website on Github">
            <i class="fa fa-github"></i><div class="githubname">{{ site.github_user }}/{{ site.github_repo }}</div>
        </a>
       <!-- <a href=""><input class="button" type="submit" value="See Progress" /></a>
        <a href="./news/"><input class="button" type="submit" value="Dev News" /></a>-->
    </div>
</div>