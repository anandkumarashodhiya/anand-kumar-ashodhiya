---
layout: default
title: "Articles data audit"
sitemap: false
---

| Slug | Page | DOI on page | published | PDF file | citation.pdf | yml title | page short_title |
|---|---|---|---|---|---|---|---|
{% for s in site.data.articles %}{% for a in s.items -%}
{%- capture a_url %}/articles/{{ a.slug }}.html{% endcapture -%}
{%- capture a_pdf %}/articles/{{ a.slug }}.pdf{% endcapture -%}
{%- assign ap = site.pages | where: "url", a_url | first -%}
{%- assign pf = site.static_files | where: "path", a_pdf | first -%}
| {{ a.slug }} | {% if ap %}✅{% else %}❌{% endif %} | {% if ap.citation.doi.size > 0 %}✅ {{ ap.citation.doi }}{% else %}❌{% endif %} | {% if ap.citation.published %}✅{% else %}❌{% endif %} | {% if pf %}✅{% else %}❌{% endif %} | {% if ap.citation.pdf == a_pdf %}✅{% else %}❌ {{ ap.citation.pdf }}{% endif %} | {{ a.title }} | {{ ap.citation.short_title }} |
{% endfor %}{% endfor %}
