---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Post
permalink: /post/
---

{% for post in site.posts %}

<div class="post-preview-container">
  <article>
  <a  class="clicable" href="{{ post.url }}">
  <div class="post-preview-title">
    <h2>
      <!-- <a href="{{ post.url }}"> -->
        {{ post.title }}
      <!-- </a> -->
    </h2>
    </div>
    <div class="post-preview-date">
    <time datetime='{{ post.date | date: "%Y-%m-%d" }}'>{{ post.date | date_to_long_string }}</time> - {{post.content |
  number_of_words | divided_by:180 }} mins</div>
    <div class="post-preview-excerpt">
    {{ post.excerpt | strip_html | truncate: 256  }}...
    </div>
      </a>

  </article></div>
{% endfor %}
