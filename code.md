---
layout: page
title: Code
permalink: /code/
---

{% assign code_posts = site.categories.code | sort: 'date' | reverse %}

{% if code_posts and code_posts.size > 0 %}
<ul>
{% for post in code_posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span class="post-meta">{{ post.date | date: site.minima.date_format | default: "%b %-d, %Y" }}</span>
  </li>
{% endfor %}
</ul>
{% else %}
<p>No code posts yet.</p>
{% endif %}

