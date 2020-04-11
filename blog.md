---
layout: default
---

<table>
  {% for post in site.posts %}
    <tr>
      <td><h3><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h3></td>
      <td class="date">{{ post.date | date: '%B %d, %Y' }}</td>
    </tr>

  {% endfor %}
</table>
