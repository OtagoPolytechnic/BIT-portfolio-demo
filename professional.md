---
layout: page
title: Professional
nav: true
---
This page is for showing evidence of professionalism in my work. Like the [Projects](projects.html) page, it's a landing page for a collection of posts.

This should be a list of professional posts:
<ul class="post-list">
    {% for post in site.categories.professional %}
      <li>
        {% assign date_format = site.minima.date_format | default: "%b %-d, %Y" %}
        <span class="post-meta">{{ post.date | date: date_format }}</span>

        <h2>
          <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
        </h2>
      </li>
    {% endfor %}
  </ul>