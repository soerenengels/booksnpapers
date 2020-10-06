---
title: Archiv
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

— zur [Session]({{ book.sessionlink }}) / zur [Ankündigung]({{ book.permalink }})

</div>

</section>

{% endfor %}
