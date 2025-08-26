---
layout: page
title: Non-Fiction
permalink: /non-fiction/
---

{% assign nf_posts = site.categories["non-fiction"] | sort: 'date' | reverse %}

{% if nf_posts and nf_posts.size > 0 %}
<ul>
{% for post in nf_posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span class="post-meta">{{ post.date | date: site.minima.date_format | default: "%b %-d, %Y" }}</span>
  </li>
{% endfor %}
</ul>
{% else %}
<p>No non-fiction posts yet.</p>
{% endif %}

