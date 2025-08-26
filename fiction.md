---
layout: page
title: Fiction
permalink: /fiction/
---

{% assign fiction_posts = site.categories.fiction | sort: 'date' | reverse %}

{% if fiction_posts and fiction_posts.size > 0 %}
<ul>
{% for post in fiction_posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span class="post-meta">{{ post.date | date: site.minima.date_format | default: "%b %-d, %Y" }}</span>
  </li>
{% endfor %}
</ul>
{% else %}
<p>No fiction posts yet.</p>
{% endif %}

