---
layout: post
title: Co-Op Trail Map
nav-menu: true
show_tile: false
---

{% assign mytiles = site.posts | where_exp: "item", "item.route == true" %}


<p>This is a map of the segments we have worked on so far. Click on a segment to go to the detailed directions and documentary series for each, or view below for each segment description.</p>

<div class="iframeholder"><iframe width="100%" id="map" frameborder="0" allowfullscreen src="//umap.openstreetmap.fr/en/map/co-op-trail_531479?scaleControl=false&miniMap=false&scrollWheelZoom=false&zoomControl=true&allowEdit=false&moreControl=true&searchControl=null&tilelayersControl=null&embedControl=null&datalayersControl=true&onLoadPanel=undefined&captionBar=false"></iframe></div><p><a href="//umap.openstreetmap.fr/en/map/co-op-trail_531479">See full screen</a></p>

<section id="two" class="spotlights">
    <h2 style="margin-top:5%;text-align:center;">Trail Segments</h2>
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

