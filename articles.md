---
layout: page
title: Articles
permalink: /articles/
---

<section class="post-list">
{% for post in site.categories['articles'] %}
<h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <p class="post-meta"><time class="archive_list_post_date" datetime='{{post.date | date: "%Y-%m-%d"}}'>{{ post.date | date_to_string }}</time> — {% for tag in post.tags %} <a class="tag_list_link" href="/tag/{{ tag }}">{{ tag }}</a>{% if forloop.last == false %},{% endif %} {% endfor %}</p>
{% endfor %}
</section>