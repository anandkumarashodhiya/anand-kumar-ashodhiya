---
layout: default
title: "Research Publications"
description: "Scholarly publications of Anand Kumar Ashodhiya on Haryanvi Ragni literature, Pingal Shastra, folk poetics, oral traditions and vernacular philosophy, with DOIs and links to the published versions."
permalink: /publications.html
image: /og-image.jpg
last_modified_at: 2026-10-08
---

{% include profile-header.html %}
{%- assign total = 0 -%}
{%- assign doi_count = 0 -%}
{%- for s in site.data.articles -%}
  {%- for a in s.items -%}
    {%- assign total = total | plus: 1 -%}
    {%- capture a_url -%}/articles/{{ a.slug }}.html{%- endcapture -%}
    {%- assign ap = site.pages | where: "url", a_url | first -%}
    {%- if ap.citation.doi.size > 0 -%}{%- assign doi_count = doi_count | plus: 1 -%}{%- endif -%}
  {%- endfor -%}
{%- endfor %}

# Research Publications

**Anand Kumar Ashodhiya**, independent researcher and former Warrant Officer, Indian Air Force.

This archive lists the scholarly articles of Anand Kumar Ashodhiya on Haryanvi Ragni literature, Pingal Shastra, Saang-Shaili traditions, vernacular poetics, oral-performance aesthetics, folk philosophy and North Indian oral literary systems. The articles examine prosody, Chhand architecture, Guru-Laghu sequencing, Yati structure, Bhakti aesthetics, folk hermeneutics, cultural memory and oral epistemology.

## Overview

- **Articles listed:** {{ total }}
- **Articles with a registered DOI:** {{ doi_count }} of {{ total }}
- **Languages:** Hindi and English
- **Journals and platforms:** IJCRT, JETIR, IJRAR, RESEARCH REVIEW, ShodhPatra, IJIRT, The Academic, International Journal of Hindi Research
- **Archives:** Zenodo, Academia.edu, ORCID, OpenAIRE

Where a journal assigns its own DOI it is labelled "DOI (journal)". Where the published open-access PDF has been deposited in Zenodo, the DOI identifies that archived copy and is labelled "DOI (Zenodo archive)".

{% for s in site.data.articles %}
## {{ s.series }}

{% for a in s.items -%}
{%- capture a_url %}/articles/{{ a.slug }}.html{% endcapture -%}
{%- assign ap = site.pages | where: "url", a_url | first -%}
{%- assign c = ap.citation -%}
{%- assign d = c.doi -%}
{%- assign links = site.data.publication_links[a.slug] %}
- **{{ c.title }}**<br>
  {{ c.journal }}{% if c.volume %}, {{ c.volume }}({{ c.issue }}){% endif %}{% if c.firstpage %}, pp. {{ c.firstpage }}–{{ c.lastpage }}{% endif %} ({{ c.published | date: "%Y" }})<br>
  [Article page]({{ a_url | relative_url }}){% if d.size > 0 %} · {% if d contains "10.5281/zenodo" %}DOI (Zenodo archive){% else %}DOI (journal){% endif %}: [{{ d }}](https://doi.org/{{ d }}){% if d contains "10.5281/zenodo" %} · [Zenodo record](https://zenodo.org/records/{{ d | remove: "10.5281/zenodo." }}){:target="_blank" rel="noopener noreferrer"}{% endif %}{% endif %}{% if links.publisher %} · [Journal version]({{ links.publisher }}){:target="_blank" rel="noopener noreferrer"}{% endif %}{% if links.academia %} · [Academia.edu]({{ links.academia }}){:target="_blank" rel="noopener noreferrer"}{% endif %}
{% endfor %}
{% endfor %}

## Major research domains

Pingal Shastra and Indian prosody · Haryanvi Ragni oral traditions · Saang-Shaili folk performance systems · North Indian oral literature · Bhakti aesthetics and vernacular devotional consciousness · folk hermeneutics and oral epistemology · cultural semiotics and folk sociology · cultural anxiety and ethical selfhood · vernacular philosophy and Vedantic folk expression · oral poetics and mnemonic structures · narrative performance and Chhand architecture

## Scholarly commentary and literary essays

Supplementary essays and prosodic commentary published on Medium:

- [Structural Continuity and Thematic Development in Adharajan Ragnis](https://medium.com/@ashodhiya68/structural-continuity-and-thematic-development-in-adharajan-ragnis-e2a5340225e8){:target="_blank" rel="noopener noreferrer"}
- [Climactic Resolution and Metrical Closure in Heer–Ranjha Ragnis](https://medium.com/@ashodhiya68/climactic-resolution-and-metrical-closure-in-heer-ranjha-ragnis-b0e370f31165){:target="_blank" rel="noopener noreferrer"}
- [Expanding Narrative Complexity in Heer–Ranjha: A Prosodic Perspective](https://medium.com/@ashodhiya68/expanding-narrative-complexity-in-heer-ranjha-a-prosodic-perspective-f4789340e755){:target="_blank" rel="noopener noreferrer"}
- [Narrative Ethics and Prosodic Form in Bhagat Puranmal Ragnis](https://medium.com/@ashodhiya68/narrative-ethics-and-prosodic-form-in-bhagat-puranmal-ragnis-8e4393c4845b){:target="_blank" rel="noopener noreferrer"}
- [Reframing Haryanvi Ragni Through Pingal Prosody](https://medium.com/@ashodhiya68/reframing-haryanvi-ragni-through-pingal-prosody-insights-from-adharajan-d20e74b00145){:target="_blank" rel="noopener noreferrer"}
- [Metrical Discipline in Heer–Ranjha Ragnis](https://medium.com/@ashodhiya68/metrical-discipline-in-heer-ranjha-ragnis-a-pingal-based-reading-b8d594785db4){:target="_blank" rel="noopener noreferrer"}
- [हरयाणवी रागणी 4: हरियाणे में व्याप्त कुरीति — पिंगल विश्लेषण](https://medium.com/@ashodhiya68/हरयाणवी-रागणी-4-हरियाणे-में-व्याप्त-कुरीति-पिंगल-विश्लेषण-88032e9977d6){:target="_blank" rel="noopener noreferrer" lang="hi"}
- [Ath Marjarika Uvach: The Great Battle of Indian History](https://medium.com/@ashodhiya68/ath-marjarika-uvach-the-great-battle-of-indian-history-867cb87268ae){:target="_blank" rel="noopener noreferrer"}
- [From Protector of the Skies to Preserver of Culture](https://medium.com/@ashodhiya68/from-protector-of-the-skies-to-preserver-of-culture-the-literary-odyssey-of-anand-kumar-ashodhiya-903d75ffd290){:target="_blank" rel="noopener noreferrer"}

**WorldCat catalogue:** [The Complete Works of Anand Kumar Ashodhiya](https://search.worldcat.org/lists/e6a2d641-2e18-4299-aaff-7697fd62c8b1){:target="_blank" rel="noopener noreferrer"}

[← Back to Home]({{ '/' | relative_url }})

{% include wiki-links.md %}

{% include footer.html %}
