---
layout: default
title: Blog
cover:
  img: hiragana.jpg
  license: (CC BY 2.0)
  reference: https://www.flickr.com/photos/45598444@N07/4289002444/                                                                                                         
---

<div class="content" id="home">
  <div id="sidebar-button">
    <img src="/images/sidebar-button.png">
  </div>
  <div id="post-info">
    <div id="cover-photo-container">
      <img id="cover-photo" src="/images/{{ page.cover.img }}" alt="{{ page.cover.reference }} {{ page.cover.license }}">
    </div>
    <div id="info-container">
      <h1 id="title">{{ page.title }}</h1>
    </div>
  </div>

  {% for post in site.posts %}
    <div class='post-list'>
      <p>
        <a class="post-title" href="{{ post.url }}">
          <span class="post-date">{{ post.date | date_to_string }}</span>
          {{ post.title }}
        </a>
      </p>
      <p>
        {{ post.summary }}
      </p>
    </div>
  {% endfor %}
</div>
