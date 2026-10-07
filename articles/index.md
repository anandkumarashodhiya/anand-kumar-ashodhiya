---
layout: default
title: "Research Articles on Haryanvi Ragni and Pingal Shastra"
description: "Research articles by Anand Kumar Ashodhiya on Haryanvi Ragni, Pingal Shastra, Saang-Shaili traditions, oral poetics, folk philosophy and vernacular literary criticism."
image: /og-image.jpg
last_modified_at: 2026-10-07
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
  "author": { "@id": "{{ '/' | absolute_url }}#person" },
  "mainEntity": {
    "@type": "ItemList",
    "numberOfItems": {{ total }},
    "itemListElement": [
{%- assign pos = 0 -%}
{%- for s in site.data.articles -%}
{%- for a in s.items -%}
{%- assign pos = pos | plus: 1 %}
      {
        "@type": "ListItem",
        "position": {{ pos }},
        "name": {{ a.title | jsonify }},
        "url": "{{ '/articles/' | append: a.slug | append: '.html' | absolute_url }}"
      }{% unless pos == total %},{% endunless -%}
{%- endfor -%}
{%- endfor %}
    ]
  }
}
</script>
{:/nomarkdown}

# Research Articles

This archive collects the scholarly articles of **Anand Kumar Ashodhiya** on **Haryanvi Ragni**, **Pingal Shastra**, **Saang-Shaili oral traditions**, vernacular poetics, folk dramaturgy, ethical consciousness and North Indian performance literature.

The articles examine metrical architecture, Guru-Laghu sequencing, Yati systems, oral cadence, refrain structures, Bhakti aesthetics, narrative ethics, cultural memory and vernacular philosophy in contemporary Haryanvi literary traditions.

## Research overview

- **Articles listed:** {{ total }}
- **Articles with a registered DOI:** {{ doi_count }} of {{ total }} ({{ journal_count }} journal DOIs, {{ zen_count }} Zenodo archive DOIs)
- **Languages:** Hindi and English
- **Core methods:** Pingal prosody, oral tradition studies, folk-performance theory, cultural semiotics, vernacular philosophy
- **Publishing platforms:** IJCRT, JETIR, IJRAR, The Academic, RESEARCH REVIEW, ShodhPatra, IJIRT, IJHR
- **Archives and profiles:** Zenodo, Academia.edu, ORCID, OpenAIRE

{% for s in site.data.articles %}
## {{ s.series }}

{{ s.intro }}

{% for a in s.items -%}
{%- capture a_url %}/articles/{{ a.slug }}.html{% endcapture -%}
{%- assign ap = site.pages | where: "url", a_url | first -%}
{%- assign d = ap.citation.doi -%}
{%- assign dl = "" -%}
{%- if d.size > 0 -%}{%- if d contains "10.5281/zenodo" -%}{%- assign dl = "DOI (Zenodo archive)" -%}{%- else -%}{%- assign dl = "DOI (journal)" -%}{%- endif -%}{%- endif %}
- [**{{ a.title }}**]({{ a_url | relative_url }})<br>
  {{ a.summary }}<br>
  {% if d.size > 0 %}{{ dl }}: [{{ d }}](https://doi.org/{{ d }}) · {% endif %}[PDF]({{ '/articles/' | append: a.slug | append: '.pdf' | relative_url }}){: aria-label="PDF: {{ a.title }}"}
{% endfor %}
{% endfor %}

## Core research domains

Pingal Shastra (Indian prosody) · Haryanvi Ragni tradition · Saang-Shaili performance systems · oral tradition and folk memory · folk hermeneutics and vernacular philosophy · Bhakti aesthetics and ethical literature · North Indian oral poetics · performative literary theory · cultural semiotics and folk psychology · vernacular metaphysics and ethical selfhood

## Scholarly orientation

This research programme seeks to establish Haryanvi Ragni literature as a field of advanced literary and interdisciplinary scholarship, through systematic engagement with Pingal metrics, oral-performance traditions, folk aesthetics, vernacular epistemology and ethical discourse.

- [Complete publications index]({{ '/publications.html' | relative_url }})
- [Citations and academic impact]({{ '/citations.html' | relative_url }})
- [Books and bibliography]({{ '/books.html' | relative_url }})

## About the DOIs

Where a journal assigns its own DOI, it is shown as "DOI (journal)". Where the published open-access PDF has been deposited in the Zenodo repository, the DOI identifies that archived copy and is shown as "DOI (Zenodo archive)". Both are permanent, citable identifiers.

## Scholarly commentary and literary essays

Supplementary essays, research reflections and prosodic commentary published on Medium:

- [Structural Continuity and Thematic Development in Adharajan Ragnis](https://medium.com/@ashodhiya68/structural-continuity-and-thematic-development-in-adharajan-ragnis-e2a5340225e8){:target="_blank" rel="noopener noreferrer"}
- [Climactic Resolution and Metrical Closure in Heer–Ranjha Ragnis](https://medium.com/@ashodhiya68/climactic-resolution-and-metrical-closure-in-heer-ranjha-ragnis-b0e370f31165){:target="_blank" rel="noopener noreferrer"}
- [Expanding Narrative Complexity in Heer–Ranjha: A Prosodic Perspective](https://medium.com/@ashodhiya68/expanding-narrative-complexity-in-heer-ranjha-a-prosodic-perspective-f4789340e755){:target="_blank" rel="noopener noreferrer"}
- [Narrative Ethics and Prosodic Form in Bhagat Puranmal Ragnis](https://medium.com/@ashodhiya68/narrative-ethics-and-prosodic-form-in-bhagat-puranmal-ragnis-8e4393c4845b){:target="_blank" rel="noopener noreferrer"}
- [Reframing Haryanvi Ragni Through Pingal Prosody](https://medium.com/@ashodhiya68/reframing-haryanvi-ragni-through-pingal-prosody-insights-from-adharajan-d20e74b00145){:target="_blank" rel="noopener noreferrer"}
- [Metrical Discipline in Heer–Ranjha Ragnis](https://medium.com/@ashodhiya68/metrical-discipline-in-heer-ranjha-ragnis-a-pingal-based-reading-b8d594785db4){:target="_blank" rel="noopener noreferrer"}
- [हरयाणवी रागणी 4: हरियाणे में व्याप्त कुरीति — पिंगल विश्लेषण](https://medium.com/@ashodhiya68/हरयाणवी-रागणी-4-हरियाणे-में-व्याप्त-कुरीति-पिंगल-विश्लेषण-88032e9977d6){:target="_blank" rel="noopener noreferrer" lang="hi"}
- [Ath Marjarika Uvach: The Great Battle of Indian History](https://medium.com/@ashodhiya68/ath-marjarika-uvach-the-great-battle-of-indian-history-867cb87268ae){:target="_blank" rel="noopener noreferrer"}
- [From Protector of the Skies to Preserver of Culture](https://medium.com/@ashodhiya68/from-protector-of-the-skies-to-preserver-of-culture-the-literary-odyssey-of-anand-kumar-ashodhiya-903d75ffd290){:target="_blank" rel="noopener noreferrer"}

## Technical research documentation

For prosodic methodologies, bibliographic records and glossaries, see the project Wiki:

- [Research Wiki Home](https://github.com/anandkumarashodhiya/anand-kumar-ashodhiya/wiki){:target="_blank" rel="noopener noreferrer"} — research mission and project overview
- [Pingala Shastra Methodology](https://github.com/anandkumarashodhiya/anand-kumar-ashodhiya/wiki/Pingala-Shastra-Methodology-in-Haryanvi-Ragni){:target="_blank" rel="noopener noreferrer"} — technical framework for Pingal-based Ragni analysis
- [Bibliography & Research Index](https://github.com/anandkumarashodhiya/anand-kumar-ashodhiya/wiki/Bibliography%E2%80%90and%E2%80%90Research){:target="_blank" rel="noopener noreferrer"} — books and DOI-indexed research papers
- [Glossary of Haryanvi Prosodic Terms](https://github.com/anandkumarashodhiya/anand-kumar-ashodhiya/wiki/Glossary%E2%80%90of%E2%80%90Haryanvi%E2%80%90Prosodic%E2%80%90Terms){:target="_blank" rel="noopener noreferrer"} — terminology of Pingal prosody and oral metrics

## Preservation and accessibility

The articles are linked to archival repositories, DOI systems and publisher databases to support long-term preservation and citation continuity. See also the [WorldCat catalogue: The Complete Works of Anand Kumar Ashodhiya](https://search.worldcat.org/lists/e6a2d641-2e18-4299-aaff-7697fd62c8b1){:target="_blank" rel="noopener noreferrer"}.

[← Return to Home]({{ '/' | relative_url }})

{% include footer.html %}
