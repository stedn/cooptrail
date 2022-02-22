---
layout: page
title: Journey Hubs
description: Find cycling routes and ideas for regenerative travel based around local hub cities, incluidng bike overnights, hiking, backpacking, bike-to-hike and volunteering.
nav-menu: true
show_tile: true
hide_image: true
image: assets/images/hubmap_cool.png
---

{% assign mytiles = site.html_pages | where_exp: "item", "item.layout == 'hub'" %}


<p>We're building the Trail Cooperative around regional hubs to help <a href="story.html">foster communities</a> dedicated to <a href="regenerative-travel.html">regenerative travel</a>. Click on a region for routes and resources on regenerative travel in that area.  To view a specific resource nationwide, check out our <a href="resources.html">resource maps page</a>. </p>

<div class="iframeholder"><iframe width="100%" id="map" frameborder="0" allowfullscreen src="//umap.openstreetmap.fr/en/map/trail-cooperative-overview_684823?scaleControl=false&miniMap=false&scrollWheelZoom=false&zoomControl=true&allowEdit=false&moreControl=true&searchControl=null&tilelayersControl=null&embedControl=null&datalayersControl=true&onLoadPanel=undefined&captionBar=false"></iframe></div><p><a href="//umap.openstreetmap.fr/en/map/trail-cooperative-overview_684823">See full screen</a></p>

<section id="two" class="spotlights">
    <h2 style="margin-top:5%;text-align:center;">Trail Regions</h2>
    {% for tile in mytiles reversed %}
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
                <p>{{ tile.description }}</p>
                <ul class="actions">
                    <li><a href="{{ tile.url  | relative_url }}" class="button">Learn more</a></li>
                </ul>
            </div>
        </div>
    </section>
    {% endfor %}
</section>

