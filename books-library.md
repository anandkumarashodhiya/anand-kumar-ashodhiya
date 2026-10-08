---
layout: default
title: "Books Library: Cover Gallery"
description: "Visual catalogue and cover gallery of the published books of Anand Kumar Ashodhiya in Haryanvi, Hindi and English."
permalink: /books-library.html
image: /adhrajan-cover.jpg
last_modified_at: 2026-10-08
---

{% include profile-header.html %}

# Books Library

A visual catalogue of the published works of **Anand Kumar Ashodhiya**. Select a cover or title for details.

{% for b in site.data.books -%}
{%- capture b_url %}/books/{{ b.slug }}.html{% endcapture -%}
- [![{{ b.title }}, book cover]({{ b.cover | relative_url }}){: width="110"}]({{ b_url | relative_url }}) [**{{ b.title }}**]({{ b_url | relative_url }}) — {{ b.language }} · {{ b.genre }}
{% endfor %}

[View the detailed bibliography with ISBNs →]({{ '/books.html' | relative_url }})

{% include wiki-links.md %}

{% include footer.html %}
