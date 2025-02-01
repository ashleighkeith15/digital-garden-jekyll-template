---
layout: default
title: articles
permalink: /articles
---


<ul>
  {% assign article_files = site.notes | where_exp: "note", "note.path contains '/articles/'" %}
  {% for article in article_files %}
    <li>
      <a href="{{ site.baseurl }}{{ article.url }}">{{ article.title }}</a>
    </li>
  {% endfor %}
</ul>