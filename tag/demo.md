---
layout: page
title: Demo tag
---
# "Demo" blog posts

This should be a list of posts tagged "demo":
<ul class="post-list">
    {% for post in site.tags.demo %}
      <li>
        {% assign date_format = site.minima.date_format | default: "%b %-d, %Y" %}
        <span class="post-meta">{{ post.date | date: date_format }}</span>

        <h2>
          <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
        </h2>
      </li>
    {% endfor %}
  </ul>