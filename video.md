---
title: Co-op Video Interviews
layout: page
description: 'Check out our documentary series about the co-ops along the trail.'
image: assets/images/pacific_northwest/frontstreet0.jpg
nav-menu: true
hide_image: true
---
{% assign mytiles = site.posts | where_exp: "item", "item.post_type == 'coop' and item.highlight == true" %}

<!-- Main -->
<div id="main">

<section id="one">
    <div class="inner">

        <p>Below we have some highlights of the cooperative profiles that we've taken.  Browse the videos below or check out all our spotlights on our Stories Page.  And don't forget to checkout the Trail Map if you'd like to find your way along the Trail.</p>
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
