---
layout: default
permalink: /director-collector/
title: 'The Director-Collector'

---

Cockerell's fame rested - and still does - on the insatiable appetite with which he amassed treasures for his museum. His first point of call was his immediate circle of writers, artists and collectors, and the museum benefited from his capacity for nurturing life-long friendships. He cultivated new patrons too, starting with members of the University and forging new alliances with those who lacked formal Cambridge connections.

He extracted loans, gifts and bequests unparalleled in volume, value and range. He built on the Fitzwilliam's traditional strengths:  
Old Master prints, paintings, music, rare books and illuminated manuscripts (which were of special interest to him as a scholar and collector).

Through his wide interests and connections, and through his associative approach to collecting, he created new holdings too, such as literary autographs, artists' sketchbooks, Private Press editions, the works of William Blake, the Pre-Raphaelites and living artists, European and Oriental ceramics, and Japanese prints. Cockerell brought in experts as Honorary Keepers of the major collections and encouraged interest in the material among his slender staff of six - there were to be no 'fossil attendants' in his museum.

### Sir Clive Forster Cooper
{: .text-success .display-5 }
Sketched cartoon made by Sir Clive Forster Cooper presented by Leonard Holder  in 1991 (MS 788-1991)
St Cockerellius relieving a poor traveller of a manuscript
1934

Head of the Department of Zoology and a good friend of Cockerell's, Sir Clive Forster Cooper sketched this cartoon while doodling on the agenda for a Museum Syndicate meeting on 29 November 1934. The Director often entertained the Syndics with details about his latest spoils. He delighted in stories about 'the bullying and wire-pulling for which I am so justly famous.' One of the many Cambridge anecdotes about Cockerell was that a visit from him foreshadowed a wealthy man's end. While sitting in a London Club, the Duke of Devonshire received an envelope. He recognised Cockerell's hand and muttered: 'I must be dead.' A Fellow of Jesus College recalled the first words he ever heard Cockerell utter: 'So I called on the duke, he was a dying man then.'

<div class="container mb-3">
  <div class="row">
{% assign rows = site.collection.size | divided_by: 2.0 | ceil %}
{% for i in (1..rows) %}
{% assign offset = forloop.index0 | times: 2 %}
{% assign sorted = site.collection | sort:"order" %}
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
