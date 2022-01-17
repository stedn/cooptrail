---
layout: post
title: 'Regenerative Travel Resources'
description: "If you're looking to plan a regenerative travel tour, we've compiled useful resources to find the things you need.  Maps for bike co-ops, reused gear stores, food co-ops, and hiker/biker camps."
image: assets/images/bike-coop-map.png
hide_image: true
nav-menu: true
---

{% assign mytiles = site.html_pages | where_exp: "item", "item.map == true" %}

<p>Below you can find maps for resources that make regenrative travel easier, like hiker-biker camps, bike co-ops, and HikeToBike routes.</p>

<section id="two" class="spotlights">
    <h2 style="margin-top:5%;text-align:center;">Resource Maps</h2>
    {% for tile in mytiles %}
    <section>
        <a href="{{ tile.url  | relative_url }}" class="image">
            <img src="{{ tile.image }}" alt="" data-position="center center" />
        </a>
        <div class="content">
            <div class="inner">
                <header class="major">
                    <h3>
                        <a href="{{ tile.url  | relative_url }}">{{ tile.title }}</a>
                    </h3>
                </header>
                <ul class="actions">
                    <li><a href="{{ tile.url  | relative_url }}" class="button">Learn more</a></li>
                </ul>
            </div>
        </div>
    </section>
    {% endfor %}
</section>
