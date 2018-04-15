---
layout: default
title: Home
permalink: /
---

<div class="home">
  <ul class="post-list">
    {% for post in site.posts %}
      <li>
        <h1 class="post-link">
          <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h1>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
        <p>
          {{ post.excerpt }}
        </p>

        <a href="{{ post.url }}" class="read-more">Read more</a>
      </li>
    {% endfor %}
  </ul>
</div>