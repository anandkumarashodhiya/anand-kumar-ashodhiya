---
layout: default
title: "Published Works and Complete Bibliography"
description: "Complete bibliography of Anand Kumar Ashodhiya: ISBN-listed books in Haryanvi, Hindi and English on Haryanvi Ragni, Pingal Shastra, folk literature, language and history."
permalink: /books.html
image: /published-titles-by-anand-kumar-ashodhiya.jpg
last_modified_at: 2026-10-08
---

{% include profile-header.html %}

{::nomarkdown}
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "CollectionPage",
  "@id": "{{ page.url | absolute_url }}#collection",
  "url": "{{ page.url | absolute_url }}",
  "name": {{ page.title | jsonify }},
  "description": {{ page.description | jsonify }},
  "inLanguage": "en",
  "dateModified": "{{ page.last_modified_at | date_to_xmlschema }}",
  "author": { "@id": "{{ '/' | absolute_url }}#person" },
  "mainEntity": {
    "@type": "ItemList",
    "numberOfItems": {{ site.data.books.size }},
    "itemListElement": [
{%- for b in site.data.books %}
      {
        "@type": "ListItem",
        "position": {{ forloop.index }},
        "item": {
          "@type": "Book",
          "name": {{ b.title | jsonify }},
          "isbn": "{{ b.isbn | remove: '-' }}",
          "author": { "@id": "{{ '/' | absolute_url }}#person" },
          "url": "{{ '/books/' | append: b.slug | append: '.html' | absolute_url }}"
        }
      }{% unless forloop.last %},{% endunless -%}
{%- endfor %}
    ]
  }
}
</script>
{:/nomarkdown}

# Complete Bibliography

This is the list of published books by **Anand Kumar Ashodhiya** ({{ site.data.books.size }} titles). Select a title for its cover, details and where to buy it. Most titles are available through **Avikavani Publishers** on Google Play Books, Amazon and Pothi, and are catalogued in WorldCat.

| Title | Language | ISBN | Genre / form |
|---|---|---|---|
{% for b in site.data.books -%}
| [**{{ b.title }}**]({{ '/books/' | append: b.slug | append: '.html' | relative_url }}) | {{ b.language }} | {{ b.isbn }} | {{ b.genre }} |
{% endfor %}

[View the visual books library →]({{ '/books-library.html' | relative_url }})

## Research publications

For scholarly articles and analytical studies, see the [research articles]({{ '/articles/' | relative_url }}).

## Availability

![Published titles by Anand Kumar Ashodhiya]({{ '/published-titles-by-anand-kumar-ashodhiya.jpg' | relative_url }})

Buy links, cover images and ISBN details are on each book's own page.

[← Back to Home]({{ '/' | relative_url }})

{% include wiki-links.md %}

{% include footer.html %}
