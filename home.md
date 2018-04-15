---
layout: default
title: Home
permalink: /
---

<div class="home">
  <section class="post-list">
    {% for post in site.posts %}
      <!-- <h1 class="post-link">
        <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
      </h1>
      <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span> -->

      <header class="post-header">
        <h1 class="post-title">
          <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h1>
        <a class="post-meta" href="{{ page.url }}">Posted on {{ post.date | date: "%B %-d, %Y" }}</a>
      </header>

      <div class="post-content">
        {{ post.excerpt }}
      </div>

      <a href="{{ post.url }}" class="read-more">Read more</a>
    {% endfor %}
  </section>
</div>