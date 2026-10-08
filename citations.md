---
layout: default
title: "Citations and Academic Impact"
description: "Citation records, DOIs and scholarly profiles for the research of Anand Kumar Ashodhiya on Haryanvi Ragni, Pingal Shastra and Indian folk literary traditions."
permalink: /citations.html
image: /og-image.jpg
last_modified_at: 2026-10-08
---

{% include profile-header.html %}
{%- assign total = 0 -%}
{%- assign doi_count = 0 -%}
{%- assign zen_count = 0 -%}
{%- for s in site.data.articles -%}
  {%- for a in s.items -%}
    {%- assign total = total | plus: 1 -%}
    {%- capture a_url -%}/articles/{{ a.slug }}.html{%- endcapture -%}
    {%- assign ap = site.pages | where: "url", a_url | first -%}
    {%- if ap.citation.doi.size > 0 -%}
      {%- assign doi_count = doi_count | plus: 1 -%}
      {%- if ap.citation.doi contains "10.5281/zenodo" -%}
        {%- assign zen_count = zen_count | plus: 1 -%}
      {%- endif -%}
    {%- endif -%}
  {%- endfor -%}
{%- endfor -%}
{%- assign journal_count = doi_count | minus: zen_count -%}

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
    "numberOfItems": {{ total }},
    "itemListElement": [
{%- assign pos = 0 -%}
{%- for s in site.data.articles -%}
{%- for a in s.items -%}
{%- capture a_url -%}/articles/{{ a.slug }}.html{%- endcapture -%}
{%- assign ap = site.pages | where: "url", a_url | first -%}
{%- assign pos = pos | plus: 1 %}
      {
        "@type": "ListItem",
        "position": {{ pos }},
        "name": {{ ap.citation.title | default: a.title | jsonify }},
        "url": "{{ a_url | absolute_url }}"
      }{% unless pos == total %},{% endunless -%}
{%- endfor -%}
{%- endfor %}
    ]
  }
}
</script>
{:/nomarkdown}

# Citations and Academic Impact

This page lists the citation records, DOIs and scholarly profiles for the research of **Anand Kumar Ashodhiya**.

The research programme focuses on **Haryanvi Ragni tradition**, **Pingal Shastra (Indian prosody)**, **Saang-Shaili narrative systems** and **Indian folk literary studies**.

## Overview

- **Articles listed:** {{ total }}
- **Articles with a registered DOI:** {{ doi_count }} of {{ total }} ({{ journal_count }} journal DOIs, {{ zen_count }} Zenodo archive DOIs)
- **Languages:** Hindi and English
- **Primary research area:** Haryanvi Ragni literature and Pingal Shastra
- **Core domains:** folk literature, oral traditions, Saang-Shaili, Pingal prosody, cultural studies
- **Access:** full-text PDFs are openly available on each article page

Where a journal assigns its own DOI it is shown as "DOI (journal)". Where the published open-access PDF has been deposited in Zenodo, the DOI identifies that archived copy and is shown as "DOI (Zenodo archive)".

{% for s in site.data.articles %}
## {{ s.series }}

{% for a in s.items -%}
{%- capture a_url %}/articles/{{ a.slug }}.html{% endcapture -%}
{%- assign ap = site.pages | where: "url", a_url | first -%}
{%- assign c = ap.citation -%}
{%- assign d = c.doi -%}
{%- assign dl = "DOI (journal)" -%}
{%- if d contains "10.5281/zenodo" -%}{%- assign dl = "DOI (Zenodo archive)" -%}{%- endif -%}
### {{ c.title }}

**Journal:** {{ c.journal }}{% if c.volume %}, {{ c.volume }}({{ c.issue }}){% endif %}{% if c.firstpage %}, pp. {{ c.firstpage }}–{{ c.lastpage }}{% endif %}

{% if d.size > 0 %}**{{ dl }}:** [https://doi.org/{{ d }}](https://doi.org/{{ d }}){:target="_blank" rel="noopener noreferrer"}
{% endif %}
**Suggested citation (APA):** Ashodhiya, A. K. ({{ c.published | date: "%Y" }}). *{{ c.title }}*. {{ c.journal }}{% if c.volume %}, {{ c.volume }}({{ c.issue }}){% endif %}{% if c.firstpage %}, {{ c.firstpage }}–{{ c.lastpage }}{% endif %}.{% if d.size > 0 %} https://doi.org/{{ d }}{% endif %}

**Research focus:** {{ c.keywords | join: ", " }}

[Read the article page]({{ a_url | relative_url }})

{% endfor %}
{% endfor %}

## Academic indexing and scholarly profiles

- [Google Scholar profile](https://scholar.google.com/citations?user=mO9WCuIAAAAJ){:target="_blank" rel="noopener noreferrer"}
- [ORCID researcher profile](https://orcid.org/0009-0005-1592-0592){:target="_blank" rel="noopener noreferrer"}
- [Zenodo open research archive](https://zenodo.org/search?q=metadata.creators.person_or_org.name:%22Ashodhiya,%20Anand%20Kumar%22){:target="_blank" rel="noopener noreferrer"}
- [OpenAIRE](https://explore.openaire.eu/search/advanced/research-outcomes?f0=resultauthor&fv0=ANAND%20KUMAR%20ASHODHIYA){:target="_blank" rel="noopener noreferrer"}
- [Academia.edu profile](https://independent.academia.edu/AAshodhiya){:target="_blank" rel="noopener noreferrer"}
- [WorldCat catalogue: The Complete Works of Anand Kumar Ashodhiya](https://search.worldcat.org/lists/e6a2d641-2e18-4299-aaff-7697fd62c8b1){:target="_blank" rel="noopener noreferrer"}
- [ISNI international author identifier](https://isni.org/isni/0000000530187854){:target="_blank" rel="noopener noreferrer"}

## Academic contribution

The research corpus contributes to the study of Haryanvi folk literature through a structured Pingal-based analytical method. It aims to preserve, document and critically interpret oral literary traditions.

- Technical analysis of Chhand-Vidhan and Matra-Santulan
- Documentation of Haryanvi Ragni prosodic systems
- Critical interpretation of Saang-Shaili narrative traditions
- Bridging oral traditions with literary criticism
- Open-access folk literature research
- A structured folk-literary research methodology

## Primary source texts

These books are published under **Avikavani Publishers**, the author's own self-publishing imprint ([about the imprint]({{ '/publishers.html' | relative_url }})).

- [Adhirājan — Folk Epic (Revised Edition)]({{ '/books/adhirajan-edition-2.html' | relative_url }})
- [Heer–Ranjha — Haryanvi Folk Narrative]({{ '/books/heer-ranjha.html' | relative_url }})
- [Kissa Bhagat Puranmal — Folk Moral Narrative]({{ '/books/kissa-bhagat-puranmal.html' | relative_url }})
- [Antaryātrā — Poetry and Reflective Literary Work]({{ '/books/antaryatra.html' | relative_url }})
- [Complete bibliography with ISBNs]({{ '/books.html' | relative_url }})

{% include wiki-links.md %}

[← Back to Home]({{ '/' | relative_url }})

{% include footer.html %}
