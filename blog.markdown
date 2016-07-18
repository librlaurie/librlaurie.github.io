---
layout: page
title: Blog
permalink: /blog/
---

<ul class="post-list">
  {% for post in site.posts %}
    <li>{{ post.date | date: "%b %-d, %Y" }}
      <h3>
        <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
      </h3>
      {{ post.excerpt | remove: '<p>' | remove: '</p>' }}
    </li>
    <hr/>
  {% endfor %}
</ul>

<p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>
