---
layout: page
title: Books
permalink: /books/
---

<section class="post-list">
  {% for post in site.categories['books'] %}
  <div class="cf">
    <a href="{{ post.url }}"><img alt="{{ post.title }} book cover" src="/assets/images/{{post.image}}.jpg" class="floatLeft" width="120"></a>
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <p class="no-margin">By Matej Latin</p>
    <small class="post-meta"><time class="archive_list_post_date" datetime='{{post.date | date: "%Y-%m-%d"}}'>{{ post.date | date_to_string }}</time> — {% for tag in post.tags %} <a class="tag_list_link" href="/tag/{{ tag | downcase }}/">{{ tag }}</a>{% if forloop.last == false %},{% endif %} {% endfor %}</small>
  </div>
  {% endfor %}
  <div class="cf">
    <img alt="Coding for Designers book cover" src="/assets/images/bwtds-cover.jpg" class="floatLeft" width="120">
    <h2>Better web typography for design&nbsp;systems</h2>
    <p class="no-margin">By Matej Latin</p>
    <small class="post-meta">Coming in 2020 — <a class="tag_list_link" href="/tag/typography/">Typography</a>, <a class="tag_list_link" href="/tag/front-end/">Front-end</a>, <a class="tag_list_link" href="/tag/web-design/">Web-design</a>, <a class="tag_list_link" href="/tag/books/">Books</a></small>
  </div>
  <!-- <div class="cf">
    <img alt="Coding for Designers book cover" src="/assets/images/cfd-cover.jpg" class="floatLeft" width="120">
    <h2>Coding for designers</h2>
    <p class="no-margin">By Matej Latin</p>
    <small class="post-meta">Coming in 2019 — <a class="tag_list_link" href="/tag/front-end/">Front-end</a>, <a class="tag_list_link" href="/tag/web-design/">Web-design</a>, <a class="tag_list_link" href="/tag/books/">Books</a></small>
  </div> -->
</section>
