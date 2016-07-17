---
layout: page
title: About
permalink: /about/
---

## About Laurie
I am the Assistant Director for Digital Scholarship at the Penn Libraries.
![laurie talks](/assets/images/Laurie-talky.jpg){: .img-responsive .text-right .img-square}

<ul class="post-list">
  {% for post in site.posts %}
    <li>{{ post.date | date: "%b %-d, %Y" }}
      <h3>
        <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
      </h3>
    </li>
  {% endfor %}
</ul>

<p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>



## About the header image
The image at the top of these pages is from the Philadelphia City Planning Commission Northwest District Plan of 1966. The full plan (and map) are available on the [Philadelphia Neighborhoods Plans](http://sceti.library.upenn.edu/pages%20/index.cfm?so_id=5923) website. Re-doing that site is something that I've wanted to do since it was created in the mid-2000s. I find the plans there incredibly fascinating and scary and sad and strange. The interface, however, does not do them justice in 2016. So, we're working on a new one now that I'm back at the Penn Libraries.

**Why this one in particular?**
I chose the Northwest Plan for lots of reasons. First, and most obviously, because I grew up in the part of the city pictured above. My family lived in Germantown, in Awbury Arboretum for the first 8 years of my life, which is at the south east part of this map. Then, we moved north and west into Mt. Airy, also pictured here. Also, though, I just love the aesthetics of these maps. Here's the key:
[![Land use](/assets/images/small-key-land-use.png)](http://sceti.library.upenn.edu/pages%20/index.cfm?so_id=5923&PagePosition=21&level=1)

This way of reading and representing my home seems so much more real to me than the way you see in Google maps.

Also, and probably not coincidentally, my father worked for the City Planning Commission in the late 1970's and early 1980's until his death from cancer in 1983. That also probably makes me love these documents a little.
