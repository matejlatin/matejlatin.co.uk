---
layout: page
title: Articles
permalink: /articles/
---

<section class="post-list">
{% for post in site.categories['articles'] %}
    {% assign reading_time = post.content | strip_html | number_of_words | plus:91 | divided_by:180 %}
    {% if reading_time <= 1 %}
        {% assign reading_time = '1' | append:' min read' %}
    {% else %}
        {% assign reading_time = reading_time | append:' min read' %}
    {% endif %}
<h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <p class="post-meta"><time class="archive_list_post_date" datetime='{{post.date | date: "%Y-%m-%d"}}'>{{ post.date | date_to_string }}</time>, {{ reading_time }} — {% for tag in post.tags %} <a class="tag_list_link" href="/tag/{{ tag | downcase }}/">{{ tag }}</a>{% if forloop.last == false %},{% endif %} {% endfor %}</p>
{% endfor %}
</section>