---
layout: page
title: "News & Projects"
permalink: /news.html
---

<link rel="stylesheet" href="{{ '/assets/css/styles.css' | relative_url }}">

Insights, case studies, and updates from InferSol — where we share what we've been working on and what we've learned along the way.

---

{% if site.posts.size > 0 %}
  {% for post in site.posts %}
  <div class="post-preview">
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p class="post-meta">{{ post.date | date: "%-d %B %Y" }}{% if post.tags.size > 0 %} &middot; {% for tag in post.tags %}<span class="post-tag">{{ tag }}</span>{% unless forloop.last %} {% endunless %}{% endfor %}{% endif %}</p>
    <p>{{ post.excerpt | strip_html | truncatewords: 50 }}</p>
    <a href="{{ post.url | relative_url }}" class="read-more">Read more &rarr;</a>
  </div>
  {% unless forloop.last %}<hr class="post-divider">{% endunless %}
  {% endfor %}
{% else %}
  <p>No posts yet — check back soon.</p>
{% endif %}
