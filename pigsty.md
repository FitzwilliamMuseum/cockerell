---
layout: default
permalink: /pigsty-to-palace/
title: From Pigsty to Palace
image: /images/GR.4.1919.jpg
---

Cockerell's spectacular acquisitions exacerbated the problem of space. He ensured that new collections came with funds for new galleries. In 1912 the bequest of Charles Brinsley Marlay funded Cockerell's first building campaign. Designed by Arnold Dunbar Smith and Cecil Brewer, and completed in 1924, the Marlay Galleries were praised for their innovative treatment of space and natural lighting. In 1925 Cockerell approached the wealthy and philanthropic Courtauld family.

Dunbar Smith's Courtauld wing opened in 1931 to a wide public acclaim. With the addition of a balcony to Gallery 3 in 1932 and the last extension of 1936 funded by James Stewart Henderson's bequest the Museum's space was doubled. In the meantime, the collections were trebled. Cockerell redisplayed them in chronological and geographical order, spacing out the exhibits to eliminate the 'dismal miscellany' and 'postage-stamp' clutter he had found in 1908.

He 'humanised' the galleries by introducing the 'country house' style. Fine furniture, exotic carpets and arrangements of fresh flowers recreated the aesthetic interior of a private mansion. The 'new Fitzwilliam' became a model for museums in Britain and abroad, prompting Cockerell's notorious statement: 'I found it a pigsty; I turned it into a palace.'

<div class="container mb-3">
  <div class="row">
{% assign rows = site.pigsty.size | divided_by: 2.0 | ceil %}
{% for i in (1..rows) %}
{% assign offset = forloop.index0 | times: 2 %}
{% assign sorted = site.pigsty | sort:"order" %}
    {% for author in sorted limit:2 offset:offset %}
    <div class="col-md-4 mb-3">
      <div class="card h-100" >
        <a href="{{site.url}}{{site.baseurl}}{{ author.permalink }}" class="stretched-link">
          <img class="card-img-top img-fluid" src="{{site.url}}{{site.baseurl}}{{author.image | replace: "images/", "images/thumbnails/" }}" alt="Card image cap" width="300" height="300"/>
        </a>
        <div class="card-body">
          <h3 class="lead mt-2">
            <a href="{{site.url}}{{site.baseurl}}{{ author.permalink }}" class="stretched-link">{{author.title}}</a>
          </h3>
        </div>
      </div>
    </div>
    {% endfor %}
  {% endfor %}
  </div>
</div>
