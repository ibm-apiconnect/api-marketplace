---
layout: api-standard
title: BIAN Banking APIs
description: Banking API Standards
keywords: 
duration: 
type: standard
order: 2
parent: categories/banking
---
<div class="grid-container top-pad">
  <div class="grid-x grid-margin-x" data-equalizer>
      <div class="cell">
        <a class="back-link" href="{{ site.baseurl }}/{{ page.parent }}">Back to Banking Standards</a>
      </div>
      <div class="cell">
        <h2>BIAN APIs</h2>
        <p>Banking Industry Architecture Network (BIAN) is an organization set up to establish and promote a common architectural framework for enabling banking interoperability.</p>
      </div>
      {% assign categories = site.categories | sort: 'order' %}
      {% for item in categories %}
        {% if item.type == 'api' and item.standard == 'bian' %}
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