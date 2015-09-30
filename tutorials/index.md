---
layout: page
title: Tutorials
permalink: /tutorials/
---

Here's a grab bag of topics. For a more organized approach, try a free [email course](#get_started).
<ul class="post-list">
    {% for page in site.pages %}
      {% if page.categories contains "tutorial" %}
      <li>
        <h2>
          <a class="post-link" href="{{ page.url }}">{{ page.title }}</a>
        </h2>
	<p> {{ page.excerpt }} </p>
      </li>
      {% endif %}
    {% endfor %}
</ul>
