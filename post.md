---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Post
permalink: /Post/
---

{% for post in site.posts %}

<div class="post-preview-container">
  <article>
  <div class="post-preview-title">
    <h2>
      <a href="{{ post.url }}">
        {{ post.title }}
      </a>
    </h2>
    </div>
    <div class="post-preview-date">
    <time datetime="{{ post.date | date: "%Y-%m-%d" }}">{{ post.date | date_to_long_string }}</time></div>
    <div class="post-preview-excerpt">
    {{ post.excerpt }}...
    </div>
  </article></div>
{% endfor %}
