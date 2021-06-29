---
title: Travelogues
layout: page
description: 'Tales of adventure along the Co-op Trail'
nav-menu: true
---
{% assign mytiles = site.posts | where_exp: "item", "item.log == true" %}

<!-- Main -->
<div id="main">

<section id="one">
    <div class="inner">
        <header class="major">
            <h1>Travelogues</h1>
        </header>
        <p>As maintainers travel the trail, we document our voyages.</p>
    </div>
</section>

<!-- Two -->
<section id="two" class="spotlights">
    {% for tile in mytiles %}
    <section>
        <a href="{{ tile.url  | relative_url }}" class="image" style="max-height:300px;overflow:hidden;">
            <img src="{{ tile.image }}" alt="" data-position="center center" />
        </a>
        <div class="content">
            <div class="inner">
                <header class="major">
                    <h3>{{ tile.title }}</h3>
                </header>
                <p>{{ tile.description }}</p>
                <ul class="actions">
                    <li><a href="{{ tile.url  | relative_url }}" class="button">Learn more</a></li>
                </ul>
            </div>
        </div>
    </section>
    {% endfor %}
</section>


</div>
