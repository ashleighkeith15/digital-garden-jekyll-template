---
layout: page
title: Unfinished Threads
permalink: /unfinished-threads
header_title: Works in Progress
header_excerpt: Ongoing thoughts, unfinished essays, and exploratory notes.
---

<div class="item-wrap">
{% assign thread_files = site.notes | where_exp: "note", "note.path contains '/notes/'" | where_exp: "note", "note.path contains '/articles/' != true" %}
{% for thread in thread_files %}
 <div class="item-contain">
   {% if thread.tags %}
     <div class="item-tag-wrap">
       {% for tag in thread.tags %}
         <a href="#" class="item-tag">{{ tag }}</a>
       {% endfor %}
     </div>
   {% endif %}
   
   <div class="item-content">
     <div class="title-wrap">
       <h1 class="item-title">
         <a href="{{ site.baseurl }}{{ thread.url }}">{{ thread.title }}</a>
       </h1>
     </div>
     <p class="item-excerpt">{{ thread.excerpt | strip_html | truncatewords: 30 }}</p>
   </div>
 </div>
{% endfor %}
</div>