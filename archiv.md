---
title: Archiv
layout: default
order: 3
permalink: /archiv
---

# Archiv

Die erste Session war ein großes Vergnügen. Zukünftig werden hier nach und nach die weiteren Sessions aufgelistet.

{% assign books = site.posts | where: "archiv", "true" %}

{% for book in books %}

<section markdown="1" style="margin: 1em 0; display: flex;">

<img src="{{ site.url }}/assets/{{ book.coverImage }}" alt="{{ book.coverImageAlternative }}" style="max-width: 150px">

<div style="margin: 1em;">
<h2 style="color: {{ book.color }} ;">{{ book.title }} </h2>
<p>Hier findest du <a href="https://unbias-the-news.booksnpapers.de/">den Link zur dazugehörigen Session</a>.</p>
</div>

</section>

{% endfor %}