---
layout: default
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
