---
layout: post
title: 'Regenerative Travel Resources'
description: 'maps and information to help travel better'
image: assets/images/banner.jpg
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
