---
layout: recent
title: Recent notes
---

Cheesecake biscuit toffee carrot cake jelly cookie. Toffee danish gummi bears cheesecake chupa chups cookie chocolate cake macaroon cookie. Gummi bears marzipan cotton candy pudding jelly-o soufflé chocolate bar cake.



<div class="recent-notes">
 {% assign recent_notes = site.notes | where_exp: "note", "note.path != '_notes/topics/recent-notes.md'" | sort: "date" | reverse | limit: 5 %}
 {% for note in recent_notes %}
   <div class="recent-note-preview">
     <h3 class="recent-note-title">
       <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
     </h3>
     <p class="recent-note-excerpt">{{ note.excerpt | strip_html | truncatewords: 30 }}</p>
   </div>
 {% endfor %}
</div>