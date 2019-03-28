---
layout: api-standard
title: TM Forum APIs
description: TM Forum APIs
keywords: 
duration: 
type: standard
order: 2
parent: categories/communication
---
<div class="grid-container top-pad">
  <div class="grid-x grid-margin-x" data-equalizer>
      <div class="cell">
        <a class="back-link" href="{{ site.baseurl }}/{{ page.parent }}">Back to Communications</a>
      </div>
      <div class="cell">
        <h2>TM Forum APIs</h2>
        <p>TM Forum is a non-profit industry association for service providers and their suppliers in the telecommunications industry. Members include communications and digital service providers, telephone companies, cable operators, network operators, software suppliers, equipment suppliers, systems integrators and management consultancies. Amongst other tools, they provide REST based Open APIs to help its members in their digital transformation initiatives.</p>
      </div>
      {% assign categories = site.categories | sort: 'order' %}
      {% for item in categories %}
        {% if item.type == 'api' and item.standard == 'tmforum' %}
          <div class="cell large-6 medium-12 small-12">
            <div class="card" data-equalizer-watch>
                <div class="card_content">
                  <div class="card_title">
                    <a href="{{ site.baseurl }}{{ item.url }}"><img class="api-logo" src="{{ site.baseurl }}{{ item.api-logo }}" />{{ item.title }}</a>
                  </div>
                  <p>{{ item.api-summary }}</p>
                </div>
            </div>
          </div>  
        {% endif %}
      {% endfor %}
  </div>
</div>