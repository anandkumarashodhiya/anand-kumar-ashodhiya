---
layout: default
title: "Scholarly Metadata and Citation Identity"
description: "Name variants, keywords, research domains, language tags and ISBN registry of Anand Kumar Ashodhiya, for accurate citation and indexing."
image: /og-image.jpg
last_modified_at: 2026-10-08
---

{% include profile-header.html %}

# Scholarly Metadata and Citation Identity

This page collects the metadata for the literary, research and archival work of **Anand Kumar Ashodhiya**, to support accurate citation and consistent indexing across databases.

## Standardized author identity

| Field | Value |
|---|---|
| Primary scholarly name | Anand Kumar Ashodhiya |
| Native script name | आनन्द कुमार आशोधिया |
| Literary name | Kavi Anand Shahpur |
| Professional status | Independent Researcher |
| Research domain | Haryanvi folk literature, Pingal prosody, oral traditions, translation studies |
| Nationality | Indian |

## Citation name variants

- Anand Kumar Ashodhiya
- Anand Kumar Aashodhiya
- Kavi Anand Shahpur
- आनन्द कुमार आशोधिया
- आशोधिया, आनन्द कुमार

These variants help databases and search engines connect references written in different forms and scripts.

## Research keywords

Haryanvi Ragni, Pingal Shastra, folk prosody, oral literature, Lok Chetna, Mahabharata folk tradition, indigenous poetics, folk narrative studies, Hindi translation, Haryanvi literature, regional literary systems, folk preservation, Chhand Shastra, oral tradition documentation, Indian folk studies, literary criticism, Ragni metrics, cultural preservation, vernacular literature, prosodic analysis

## Research domains

| Domain | Specialization |
|---|---|
| Folk literature | Haryanvi Ragni tradition |
| Prosody | Pingal Shastra analysis |
| Translation studies | Hindi–English literary translation |
| Cultural studies | Lok Chetna and folk consciousness |
| Digital humanities | Literary preservation and metadata structuring |

## ISBN registry

| Title | ISBN | Language |
|---|---|---|
{% for b in site.data.books -%}
| [{{ b.title }}]({{ '/books/' | append: b.slug | append: '.html' | relative_url }}) | {{ b.isbn }} | {{ b.language }} |
{% endfor %}

## Scholarly identifiers and profiles

- **ORCID:** [https://orcid.org/0009-0005-1592-0592](https://orcid.org/0009-0005-1592-0592){:target="_blank" rel="noopener noreferrer"}
- **ISNI:** [https://isni.org/isni/0000000530187854](https://isni.org/isni/0000000530187854){:target="_blank" rel="noopener noreferrer"}
- **Google Scholar:** [Scholar profile](https://scholar.google.com/citations?user=mO9WCuIAAAAJ){:target="_blank" rel="noopener noreferrer"}
- **Zenodo:** [Zenodo records by the author](https://zenodo.org/search?q=metadata.creators.person_or_org.name:%22Ashodhiya,%20Anand%20Kumar%22){:target="_blank" rel="noopener noreferrer"}
- **Amazon:** [Author page](https://www.amazon.com/author/anandkumarashodhiya){:target="_blank" rel="noopener noreferrer"}
- **Goodreads:** [Author profile](https://www.goodreads.com/author/show/58492536.Anand_Kumar_Ashodhiya){:target="_blank" rel="noopener noreferrer"}
- **MusicBrainz:** [Entity record](https://musicbrainz.org/artist/5026d6a7-cbca-4c54-b663-8673e0f10149){:target="_blank" rel="noopener noreferrer"}

## Language tags

- `en`: English
- `hi`: Hindi
- `bgc`: Haryanvi

Metadata orientation: Schema.org structured data, JSON-LD, digital preservation metadata.

## Research navigation

[Research portal]({{ '/research/' | relative_url }}) · [About the researcher]({{ '/research/about-researcher.html' | relative_url }}) · [Research interests]({{ '/research/research-interests.html' | relative_url }}) · [Academic profiles]({{ '/research/academic-profiles.html' | relative_url }}) · [Research mission]({{ '/research/research-mission.html' | relative_url }})

[← Back to Home]({{ '/' | relative_url }})

{% include footer.html %}
