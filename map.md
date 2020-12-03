---
layout: post
title: Co-Op Trail Map
description: Lorem ipsum dolor est
nav-menu: true
show_tile: false
---

{% assign mytiles = site.posts | where_exp: "item", "item.route == true" %}

<!-- <iframe style='border:none' width='100%' height='1000px'  src="https://openrouteservice.org/map/#/directions/Caspar,CA,USA/Seattle,WA,USA/Bozeman,MT,USA/Minneapolis,MN,USA/Chicago,IL,USA/Denver,CO,USA/data/55,130,32,198,15,97,4,224,38,9,96,59,2,24,5,192,166,6,113,0,184,64,90,1,24,2,96,25,128,58,0,56,0,102,180,211,8,6,148,129,57,205,32,54,82,5,96,29,152,128,220,69,139,23,106,88,181,94,140,0,178,247,33,218,135,98,132,134,19,94,90,180,226,44,200,206,239,55,169,94,28,89,9,97,88,135,14,220,184,206,158,69,151,66,164,134,83,149,113,105,25,132,170,244,162,215,149,83,65,210,143,133,146,153,141,151,154,90,133,155,133,132,17,132,2,0,1,213,30,2,17,27,7,20,5,58,2,0,12,222,0,6,221,23,28,0,19,204,24,169,0,28,223,26,29,22,160,21,216,185,26,17,36,15,61,0,189,17,177,12,12,175,0,185,19,3,12,115,160,11,202,0,22,215,16,146,128,23,209,104,0,0/embed/en-us"></iframe> -->

<p>This is a map of the segments we have worked on so far. Click on a segment to go to the detailed directions and documentary series for each, or view below for each segment description.</p>

<div class="iframeholder"><iframe width="100%" id="map" frameborder="0" allowfullscreen src="//umap.openstreetmap.fr/en/map/co-op-trail_531479?scaleControl=false&miniMap=false&scrollWheelZoom=false&zoomControl=true&allowEdit=false&moreControl=true&searchControl=null&tilelayersControl=null&embedControl=null&datalayersControl=true&onLoadPanel=undefined&captionBar=false"></iframe></div><p><a href="//umap.openstreetmap.fr/en/map/co-op-trail_531479">See full screen</a></p>

<section id="two" class="spotlights">
    {% for tile in mytiles reversed %}
    <section>
        <a href="{{ tile.url  | relative_url }}" class="image">
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

