---
layout: default
permalink: /friends/
title: The Friends of the Fitzwilliam Museum

---

While Cockerell secured major donations and bequests, he had no funds for purchases on a comparable scale. In 1909 he founded the Society of Friends of the Fitzwilliam Museum. Modelled on the Amis de Louvre, they were the first group of supporters established at a British art institution. Cockerell mobilised the local and national press to recruit members, both

>'old Cambridge men' who 'may appreciate some link other than cricket or rowing' and current undergraduates who were advised that 'fortunate coups at Newmarket should result in benefactions.'

Their annual subscriptions allowed the Director to strengthen the existing holdings, such as Turner's watercolours or the Greek vases, and to establish new collections, for instance of Blake's works and of Oriental ceramics. A century later the Friends continue to provide a strategic fund for Cockerell's successors. Their largest ever contribution was towards the purchase of the Macclesfield Psalter in 2005.

<div class="container mb-3">
  <div class="row">
{% assign rows = site.friends.size | divided_by: 2.0 | ceil %}
{% for i in (1..rows) %}
{% assign offset = forloop.index0 | times: 2 %}
{% assign sorted = site.friends | sort:"order" %}
    {% for author in sorted limit:2 offset:offset %}
    <div class="col-md-4 mb-3">
      <div class="card h-100" >
        <a href="{{site.url}}{{site.baseurl}}{{ author.permalink }}" class="stretched-link">
          <img class="card-img-top" src="{{site.url}}{{site.baseurl}}{{author.image | replace: "images/", "images/thumbnails/" }}" alt="Card image cap" width="300" height="300"/>
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
