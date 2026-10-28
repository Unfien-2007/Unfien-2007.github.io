---
title: Personal Writing
layout: page
permalink: /personal/
noindex: true
sitemap: false
---

Not everything here is technical. These pieces are more personal — journal entries and
opinions — so I keep them off the home page and out of search engine results. They're
still public and browsable if you'd like to read them.

{% assign personal_posts = site.posts | where: 'hidden', true %}
{% if personal_posts.size > 0 %}
<ul>
  {% for post in personal_posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span class="text-muted">— {{ post.date | date: "%b %-d, %Y" }}</span>
    </li>
  {% endfor %}
</ul>
{% else %}
<p class="text-muted">Nothing published yet.</p>
{% endif %}
