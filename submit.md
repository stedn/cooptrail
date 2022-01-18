---
layout: page
short_title: Submit a trip
title: Add to the community library
description: Do you have an awesome bike-to-hike trip or an organization that could help our members travel regeneratively?  Add it to one of our Journey Hub maps to share your local knowledge with regenerative travelers.
nav-menu: true
show_tile: true
hide_image: true
image: assets/images/submit.png
---

{% assign mytiles = site.html_pages | where_exp: "item", "item.layout == 'hub'" %}


<p>Click on the hubs route on the map below to go to the page where you can add your routes, organizations, or trail logs. If you don't see a hub in your area, email us (at <a href="mailto:{{ site.email }}">thecooptrail@gmail.com</a>) or contact us on <a href="{{ site.discord }}"><em>Discord</em></a> or <a href="{{ site.hylo }}"><em>Hylo</em></a> so we can set one up for you.</p>

<div class="iframeholder"><iframe width="100%" id="map" frameborder="0" allowfullscreen src="//umap.openstreetmap.fr/en/map/trail-cooperative-overview_684823?scaleControl=false&miniMap=false&scrollWheelZoom=false&zoomControl=true&allowEdit=false&moreControl=true&searchControl=null&tilelayersControl=null&embedControl=null&datalayersControl=true&onLoadPanel=undefined&captionBar=false"></iframe></div><p><a href="//umap.openstreetmap.fr/en/map/trail-cooperative-overview_684823">See full screen</a></p>
