---
layout: default
title: Главная
---

<div class="home">
  <h1 class="page-heading">Последние посты</h1>
  
  <ul class="post-list">
    {% for post in site.posts limit:5 %}
      <li>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
        <h2>
          <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
        </h2>
      </li>
    {% endfor %}
  </ul>
  
  <p class="rss-subscribe">Подписаться <a href="{{ "/feed.xml" | relative_url }}">через RSS</a></p>
</div>
