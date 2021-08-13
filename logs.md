---
title: Travel Logs
layout: page
description: 'Read highlighted routes along the Trail Cooperative'
image: assets/images/bg_map.png
nav-menu: true
---
{% assign mytiles = site.posts | where_exp: "item", "item.post_type == 'log' and item.highlight == true" %}

<!-- Main -->
<div id="main">

<section id="one">
    <div class="inner">
        <header class="major">
            <h1>Travel Log</h1>
        </header>
        <p>As maintainers travel the Trail Cooperative, we document our routes, points of interest, bike shops, campsites, resupplies points, and interesting co-ops so you can travel sustainably too.  Check out our highlighted travel logs from our US tour and see the <a href="map.html">full map</a> for all our routes and co-ops.</p>
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
