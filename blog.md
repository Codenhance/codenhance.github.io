---
layout: post
title: Blog
permalink: /blog/
---

  <ul class="post-list">
    {% for post in site.posts %}
      <li>
        <h2>
          <a class="post-link" href="{{ post.url }}">{{ post.title }}</a>
        </h2>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>

      </li>
    {% endfor %}
  </ul>
