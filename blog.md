---
layout: default
content_class: writing
---

<ul class="writing-list">
  {% for post in site.posts %}
    <li>
      <a class="writing-title" href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <time datetime="{{ post.date | date: '%Y-%m-%d' }}">{{ post.date | date: '%B %-d, %Y' }}</time>
    </li>

  {% endfor %}
</ul>
