---
layout: post
title: Recent posts
---

<ul class="post-list">
{% for post in site.posts %}
<li>
<h2>
<a class="post-link" href="{{ post.url }}">{{ post.title }}</a>
</h2>
<span class="post-meta">{{ post.excerpt }}</span>

</li>
{% endfor %}
</ul>
