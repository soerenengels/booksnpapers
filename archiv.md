---
title: "Archiv"
description: "In dem Archiv von @booksnpapers finden sich die Diskussionen und dazugehörigen Ankündigungen zu den einzelnen Lesekreis-Sessions des digitalen Journalismus-Buchclubs Books 'n Papers. Stöbere in den vergangenen Sitzungen!"
layout: default
order: 3
permalink: /archiv
---

# Archiv

Hier findest du die bisherigen Diskussionen.

{% assign books = site.posts | where: "archiv", "true" %}

{% for book in books %}

<section markdown="1" style="margin: 1em 0; display: flex;">

<img src="{{ site.url }}/assets/{{ book.coverImage }}" alt="{{ book.coverImageAlternative }}" style="max-width: 150px" loading="lazy">

<div style="margin: 1em;" markdown="1">

## {{ book.title }}

{{ book.description }}

— zur [Session]({{book.sessionlink }}) / zur [Ankündigung]({{ book.permalink }})

</div>

</section>

{% endfor %}
