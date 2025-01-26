---
layout: page
title: Noise Complaint
id: home
permalink: /
---

# Welcome! 🌱

<p style="padding: 3em 1em; background: #f5f7ff; border-radius: 4px;">
  Take a look at <span style="font-weight: bold">[[Your first note]]</span> to get started on your exploration. Hey can you see this?
</p>

This digital garden template is free, open-source, and [available on GitHub here](https://github.com/maximevaillancourt/digital-garden-jekyll-template).

The easiest way to get started is to read this [step-by-step guide explaining how to set this up from scratch](https://maximevaillancourt.com/blog/setting-up-your-own-digital-garden-with-jekyll).

<strong>Recently updated notes</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<strong>Folders</strong>

<ul>
  {% assign folders = site.notes | group_by_exp: "note", "note.path | split: '/' | reverse | drop: 1 | last" | sort: "name" %}
  {% for folder in folders %}
    <li>
      <a class="internal-link" href="{{ site.baseurl }}/{{ folder.name }}">{{ folder.name }}</a>
    </li>
  {% endfor %}
</ul>

{% include notes_graph.html %} 


<style>
  .wrapper {
    max-width: 46em;
  }
</style>
