---
layout: post
title: Test project
categories: project professional
---
This is a test post with two categories: project and professional. It should show up in the post listings on those pages.

*Post categories:* 
{% for category in page.categories %}
- {{ category }}
{%- endfor -%}
