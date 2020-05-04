---
layout: paper
title: Paper content

---
<h1>Latest Posts</h1>
<ul>
  {% for post in site.posts %}
    <li>
      <h2><a href="/master_thesis/{{ post.url }}">{{ post.title }}</a></h2>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>