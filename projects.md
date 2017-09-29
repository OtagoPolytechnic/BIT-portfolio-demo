---
layout: page
title: Projects
nav: true
---

{{ site.course_code }} Multimedia Development is assessed using four projects that make up one part of the final portfolio. This page links to a blog post for each project, showing the final output, some evidence of workflow and tool use and a short discussion about the design decisions made.

This should be a list of project posts:
<ul class="post-list">
    {% for post in site.categories.project %}
      <li>
        {% assign date_format = site.minima.date_format | default: "%b %-d, %Y" %}
        <span class="post-meta">{{ post.date | date: date_format }}</span>

        <h2>
          <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
        </h2>
      </li>
    {% endfor %}
  </ul>