---
layout: page
title: Blog
permalink: /blog/
---

<ul class="post-list">
  {% for post in site.posts %}
    <li>{{ post.date | date: "%b %-d, %Y" }}
      <h2>
        <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
      </h2>
      {{ post.excerpt | remove: '<p>' | remove: '</p>' }}
    </li>
    <a href="{{ post.url | prepend: site.baseurl }}">more...</a>
    <hr/>
  {% endfor %}
</ul>

<p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>
