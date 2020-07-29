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

<img src="{{ site.url }}/assets/{{ book.coverImage }}" alt="{{ book.coverImageAlternative }}" style="max-width: 150px">

<div style="margin: 1em;">
<h2 style="color: {{ book.color }} ;">{{ book.title }} </h2>
<p>Zur 
<a href="{{ book.sessionlink }}">Session</a>.</p>
</div>

</section>

{% endfor %}