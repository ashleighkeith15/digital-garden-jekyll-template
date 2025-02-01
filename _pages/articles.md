---
layout: default
title: articles
permalink: /articles
---



<div class="article-notes">
 {% assign article_notes = site.notes | where_exp: "note", "note.path contains 'Article'" | sort: "date" | reverse %}
 {% for note in article_notes %}
   <div class="note-preview">
     <h3 class="note-title">
       <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
     </h3>
     <p class="note-excerpt">{{ note.excerpt | strip_html | truncatewords: 30 }}</p>
   </div>
 {% endfor %}
</div>