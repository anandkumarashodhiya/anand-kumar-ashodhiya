---
layout: default
title: "Awards and Recognitions"
description: "Literary honours and recognitions received by Anand Kumar Ashodhiya for contributions to Indian literature, from 2020 to 2026, with certificates, conferring bodies and locations."
image: /og-image.jpg
last_modified_at: 2026-10-08
---

{% include profile-header.html %}
{%- assign awards = site.data.awards | where_exp: "x", "x.kind != 'other'" -%}
{%- assign others = site.data.awards | where: "kind", "other" -%}

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
  "about": { "@id": "{{ '/' | absolute_url }}#person" },
  "mainEntity": {
    "@type": "ItemList",
    "name": "Awards of Anand Kumar Ashodhiya",
    "numberOfItems": {{ awards.size }},
    "itemListElement": [
{%- for x in awards %}
      {
        "@type": "ListItem",
        "position": {{ forloop.index }},
        "item": {
          "@type": "Thing",
          "name": {{ x.title | jsonify }},
          "description": {{ x.by | append: ", " | append: x.place | append: ", " | append: x.date | jsonify }}
        }
      }{% unless forloop.last %},{% endunless -%}
{%- endfor %}
    ]
  }
}
</script>
{:/nomarkdown}

# Awards and Recognitions

Literary honours (sammans) and recognitions received by **Anand Kumar Ashodhiya** for contributions to Indian literature. {{ awards.size }} honours are listed below, newest first.

## Featured honours

| Kavi Shiromani Samman 2026 | Indian Literature Award 2026 | Haryanvi Sahitya Ratna Samman |
|:-:|:-:|:-:|
| ![Kavi Shiromani Samman 2026]({{ '/awards-gallery/kavi-shiromani-2026.jpg' | relative_url }}) | ![Indian Literature Award 2026]({{ '/awards-gallery/indian-literature-award-2026.jpg' | relative_url }}) | ![Haryanvi Sahitya Ratna Samman]({{ '/awards-gallery/haryanvi-sahitya-ratna-samman-2025.jpg' | relative_url }}) |

## Honours list

| No. | Date | Award | Conferred by | Location |
|---|---|---|---|---|
{% for x in awards -%}
| {{ forloop.index }} | {{ x.date }} | {{ x.title }} | {{ x.by }} | {{ x.place }} |
{% endfor %}

## Appointments, certificates and other recognitions

| No. | Date | Recognition | Issued by | Location |
|---|---|---|---|---|
{% for x in others -%}
| {{ forloop.index }} | {{ x.date }} | {{ x.title }} | {{ x.by }} | {{ x.place }} |
{% endfor %}

[← Back to Home]({{ '/' | relative_url }})

{% include wiki-links.md %}

{% include footer.html %}
