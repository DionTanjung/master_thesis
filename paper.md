---
layout: paper
title: Paper content

---
<ul>
  {% for post in site.posts %}
    <li>
      <h2><a href="/master_thesis/{{ post.url }}">{{ post.title }}</a></h2>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>