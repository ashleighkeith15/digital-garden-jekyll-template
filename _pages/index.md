---
layout: page
title: Noise Complaint
id: home
permalink: /
---

 <div class="content">
          <div class="content-body">
            <h1 class="u-text-h1">These are my notes.</h1>
            <p>Biscuit cotton candy toffee fruitcake danish marzipan powder gingerbread. Biscuit cotton candy toffee fruitcake danish marzipan powder gingerbread.Biscuit cotton candy toffee fruitcake danish marzipan powder gingerbread.</p>
            <div class="blockquote">
              <p>Biscuit cotton candy toffee fruitcake danish marzipan powder gingerbread. Biscuit cotton candy toffee fruitcake danish marzipan powder gingerbread.Biscuit cotton candy toffee fruitcake danish marzipan powder gingerbread.</p>
            </div>
            <a href="/about" class="button w-inline-block">
              <div class="button-label">About</div><img src="images/arrow.svg" loading="lazy" alt="" class="button-image">
            </a>
          </div>
          <div class="scattered-wrap"><img src="assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png" loading="lazy" sizes="(max-width: 767px) 125.82785034179688px, 16vw" srcset="assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png 500w, assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png 800w, assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png 1080w, assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png 1600w, assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png 2000w, assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png 2831w" alt="" class="scattered-image is-1"><img src="assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png" loading="lazy" sizes="(max-width: 767px) 128.48175048828125px, 17vw" srcset="assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png 500w, assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png 800w, assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png 1080w, assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png 1600w, assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png 2000w, assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png 2831w" alt="" class="scattered-image is-2"><img src="assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png" loading="lazy" sizes="(max-width: 479px) 128.48175048828125px, (max-width: 767px) 27vw, 17vw" srcset="assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png 500w, assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png 800w, assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png 1080w, assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png 1600w, assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png 2000w, assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png 2831w" alt="" class="scattered-image is-3"><img src="assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png" loading="lazy" sizes="(max-width: 991px) 136.2054443359375px, 18vw" srcset="assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png 500w, assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png 800w, assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png 1080w, assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png 1600w, assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png 2000w, assets/cutunseen-histories-MfkVwVm1K0w-unsplash-(1).png 2831w" alt="" class="scattered-image is-4"></div>
        </div>

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

<strong>MOCs</strong>

<ul>
  {% assign animal_notes = site.notes | where_exp: "note", "note.path contains 'animals'" %}
  {% for note in animal_notes %}
    <li>
      <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

{% include notes_graph.html %} 


<style>
  .wrapper {
    max-width: 46em;
  }
</style>
