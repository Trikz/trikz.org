---
title: Dev Logs
permalink: /devlog/
layout: post
---

<br>
<p>Subscribe with <a href="{{ site.url }}/feed.xml">RSS</a> to keep up with the latest news.
For site changes, see the <a href="https://github.com/{{ site.github_user }}/{{ site.github_repo }}/pulls?q=is%3Aclosed">closed pull requests</a> to kept up with the development!</p>

<br>

{% for post in site.posts limit:10 %}
   <div class="post-preview">
   <h2><a href="{{ site.url }}{{ post.url }}">{{ post.title }}</a></h2>
   <span class="post-date">{{ post.date | date: "%B %d, %Y" }}</span><br>
   {% if post.badges %}{% for badge in post.badges %}<span class="badge badge-{{ badge.type }}">{{ badge.tag }}</span>{% endfor %}{% endif %}
   {{ post.content | split:'<!--more-->' | first }}
   {% if post.content contains '<!--more-->' %}
      <a href="{{ site.url }}{{ post.url }}">read more</a>
   {% endif %}
   </div>
   <hr>
{% endfor %}

Want to see more? See the <a href="{{ site.url }}archive/">News Archive</a>.
