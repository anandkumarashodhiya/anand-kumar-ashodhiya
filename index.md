---
layout: default
title: "Anand Kumar Ashodhiya – Author, Poet, Researcher & Cultural Envoy"
description: "Official website of Anand Kumar Ashodhiya, author, researcher and independent scholar of Haryanvi Ragni, Pingal Shastra, Indian folk poetics, oral traditions and North Indian performance literature."
image: /og-image.jpg
last_modified_at: 2026-10-08
---

{% include profile-header.html %}

{::nomarkdown}
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "WebSite",
      "@id": "{{ '/' | absolute_url }}#website",
      "url": "{{ '/' | absolute_url }}",
      "name": "Anand Kumar Ashodhiya Official Website",
      "inLanguage": "en-IN",
      "publisher": { "@id": "{{ '/' | absolute_url }}#person" }
    },
    {
      "@type": "ProfilePage",
      "@id": "{{ '/' | absolute_url }}#profile",
      "url": "{{ '/' | absolute_url }}",
      "name": "Anand Kumar Ashodhiya | Official Biography",
      "inLanguage": "en-IN",
      "dateModified": "{{ page.last_modified_at | date_to_xmlschema }}",
      "isPartOf": { "@id": "{{ '/' | absolute_url }}#website" },
      "mainEntity": { "@id": "{{ '/' | absolute_url }}#person" }
    }
  ]
}
</script>
{:/nomarkdown}

Anand Kumar Ashodhiya is an Indian literary scholar, poet, independent researcher and former Warrant Officer of the Indian Air Force whose work focuses on Haryanvi Ragni tradition, Pingal Shastra, oral poetics, vernacular performance traditions and North Indian folk literature. His interdisciplinary scholarship integrates folk-performance studies, prosodic analysis, cultural semiotics, oral epistemology, ecological humanities, vernacular philosophy and regional literary criticism.

His published work examines Haryanvi Saang-Shaili traditions through structured analytical frameworks combining Pingal prosody, oral tradition studies, performative aesthetics, socio-cultural criticism, folk hermeneutics and regional knowledge systems.

This website is a continuously evolving research archive of scholarly articles, ISBN-linked books, oral-literary documentation, prosodic methodologies and contemporary studies in Haryanvi folk literature.

{% assign avi = site.data.articles | last %}
## Featured research: {{ avi.series }}

Recent English-language studies examining ecological anxiety, digital alienation, military folk consciousness, Viraha aesthetics, feminine trauma, cultural resistance, ethical selfhood, vernacular ethics, oral epistemology and performative poetics within contemporary Haryanvi Ragni traditions.

{% for a in avi.items -%}
{%- capture a_url %}/articles/{{ a.slug }}.html{% endcapture -%}
{%- assign ap = site.pages | where: "url", a_url | first -%}
- [**{{ a.title }}**]({{ a_url | relative_url }})<br>
  {{ ap.citation.journal_abbr | default: ap.citation.journal }}, Vol. {{ ap.citation.volume }}, Issue {{ ap.citation.issue }} ({{ ap.citation.published | date: "%Y" }})
{% endfor %}

- [Browse all research articles]({{ '/articles/' | relative_url }})
- [Publications]({{ '/publications.html' | relative_url }})
- [Citation index]({{ '/citations.html' | relative_url }})

## Research contributions

{% for s in site.data.articles %}
### {{ s.series }}

{% for a in s.items -%}
- [{{ a.title }}]({{ '/articles/' | append: a.slug | append: '.html' | relative_url }})
{% endfor %}
{% endfor %}

## Research domains

Pingal Shastra and Indian prosody · Haryanvi Ragni tradition · Saang-Shaili oral performance · North Indian folk poetics · oral tradition and folk narratology · ecological humanities · digital sociology and folk modernity · cultural anxiety and ethical selfhood studies · feminist folklore and Viraha studies · vernacular philosophy · cultural semiotics and regional knowledge systems

## Books and literary publications

- [**Heer Ranjha — Haryanvi Ragni Literary Work**]({{ '/books/heer-ranjha.html' | relative_url }})
- [**Adhirājan — Folk Epic (Revised Edition)**]({{ '/books/adhirajan-edition-2.html' | relative_url }})
- [**Kissa Bhagat Puranmal — Folk Narrative & Analysis**]({{ '/books/kissa-bhagat-puranmal.html' | relative_url }})
- [**Antaryātrā — Poetry Collection**]({{ '/books/antaryatra.html' | relative_url }})

The books and research papers on this website form a growing archive dedicated to Haryanvi Ragni literature, oral poetics, Pingal Shastra and vernacular folk-performance traditions.

- [Complete bibliography]({{ '/books.html' | relative_url }})
- [Research publications]({{ '/publications.html' | relative_url }})

## Academic profiles and research identity

- [Google Scholar](https://scholar.google.com/citations?user=mO9WCuIAAAAJ){:target="_blank" rel="noopener noreferrer"}
- [ORCID](https://orcid.org/0009-0005-1592-0592){:target="_blank" rel="noopener noreferrer"}
- [Zenodo research archive](https://zenodo.org/){:target="_blank" rel="noopener noreferrer"}
- [LinkedIn](https://www.linkedin.com/in/anand-kumar-ashodhiya-599248285){:target="_blank" rel="noopener noreferrer"}
- [YouTube channel](https://www.youtube.com/@anandragnipoint){:target="_blank" rel="noopener noreferrer"}

## Technical research documentation

For bibliographic records, Pingal methodologies and folk-literary terminology, see the project Wiki:

- [Research Wiki Home](https://github.com/anandkumarashodhiya/anand-kumar-ashodhiya/wiki){:target="_blank" rel="noopener noreferrer"} — mission and project overview
- [Pingala Shastra Methodology](https://github.com/anandkumarashodhiya/anand-kumar-ashodhiya/wiki/Pingala-Shastra-Methodology-in-Haryanvi-Ragni){:target="_blank" rel="noopener noreferrer"} — technical framework for Haryanvi Ragni analysis
- [Bibliography & Research Index](https://github.com/anandkumarashodhiya/anand-kumar-ashodhiya/wiki/Bibliography%E2%80%90and%E2%80%90Research){:target="_blank" rel="noopener noreferrer"} — DOI-registered papers and ISBN-linked publications
- [Glossary of Haryanvi Prosodic Terms](https://github.com/anandkumarashodhiya/anand-kumar-ashodhiya/wiki/Glossary%E2%80%90of%E2%80%90Haryanvi%E2%80%90Prosodic%E2%80%90Terms){:target="_blank" rel="noopener noreferrer"} — terminology of Pingal Shastra and oral-poetic traditions

## Scholarly essays and literary commentary

Supplementary essays and Pingal-centred commentary published on Medium:

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

{% include footer.html %}
