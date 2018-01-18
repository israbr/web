---
layout: page
title: Todo el mundo sabe que
permalink: /everybodyknows/
---
<div class="container">
  <header class="post-header">
    <h1 class="post-title omeya_green_color" itemprop="name headline">Todo El Mundo Sabe Que...</h1>  
  </header>
  <ul class="collection">
    {% for post in site.categories.everybodyKnows %}
      <li class="collection-item">
          <span class="title">... {{ post.sentence| escape }}.</span>
          <div>
            [+]<a class="post-link" target="_blank" href="{{ post.external_url }}"> {{ post.external_url }}</a> 
          </div>
          <div>
            <span itemprop="name"> • {{ post.author }}   
              {% if post.social and post.social_url %}
                <a class="post-link" target="_blank" href="{{ post.social_url }}"> {{ post.social }}</a>
              {% endif %}
            </span>
          </div>
      </li>
    {% endfor %}
  </ul>
</div>
