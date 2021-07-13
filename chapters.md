---
layout: default
permalink: /a-new-chapter/
title: 'A new chapter of my life'

---

The directorship of Sydney Cockerell (1908-1937) is celebrated as one of the most dynamic and enriching periods in the history of the Fitzwilliam Museum. While some Cambridge dons saw him as an outsider to academia, a self-made man without a university degree, others welcomed him as the ideal agent of reform.

A disciple of John Ruskin, William Morris and Wilfrid Blunt, Cockerell knew a wide range of styles and media, the art market of fin-du-siècle Europe, the leading artists and the most discerning private collectors of the day. He brought to Cambridge a consummate taste shaped by the Arts and Crafts and Aesthetic Movements, a shrewd business sense and sound pragmatism (sharpened by his experience in the family coal firm), wealthy patrons, boundless energy, infectious enthusiasm and a passionate belief in the role of museums as catalysts of social progress.

Cockerell transformed the Fitzwilliam Museum from a cabinet of curiosities reserved for the privileged few into a 'Palace of the Arts' open to 'all the world.'

<div class="container mb-3">
  <div class="row">
{% assign rows = site.chapters.size | divided_by: 2.0 | ceil %}
{% for i in (1..rows) %}
{% assign offset = forloop.index0 | times: 2 %}
{% assign sorted = site.chapters | sort:"order" %}
    {% for author in sorted limit:2 offset:offset %}
    <div class="col-md-4 mb-3">
      <div class="card h-100" >
        <a href="{{site.url}}{{site.baseurl}}{{ author.permalink }}" class="stretched-link">
          <img class="card-img-top" src="{{site.url}}{{site.baseurl}}{{author.image}}" alt="Card image cap" width="300" height="300"/>
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
