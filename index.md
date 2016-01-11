---
layout: page
title: Welcome to Shiftkeylabs Blog!
tagline: <br>A pre-incubator program with a relentless focus on technology.
---
We provide early-stage coaching to help you start off on the right foot. We can help you grow your network of contacts and connect you with the right people and resources to build your team and get support where it’s needed. You can also take advantage of a variety of interesting technology and business skills-building workshops. We also provide free, physical collaboration space where you can meet with your team and meet other teams who are also advancing their ideas.


<ul class="posts">
  {% for post in site.posts %}
    <li><span class="date">{{ post.date | date: '%B %d, %Y' }}</span>
    <h3><a class="post-link" href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h3>
        <p class="description">{% if post.description %}{{ post.description | strip_html | strip_newlines | truncate: 250 }}{% else %}{{ post.content | strip_html | strip_newlines | truncate: 125 }}{% endif %}</p>
    </li>
  {% endfor %}
</ul>
