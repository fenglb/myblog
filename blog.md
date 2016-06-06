---
layout: page
title : "Stay foolish stay hungry"
---
  <ul class="listing">
    {% for post in site.posts %}
      <li class="listing-item">
        <span class="post-date">{{ post.date | date: "%Y-%m-%d" }}</span>
        <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
      </li>
    {% endfor %}
  </ul>
