---
layout: default
title: Home
---

{% capture about_content %}
{% include_relative about.md %}
{% endcapture %}

{% assign content_parts = about_content | split: "---" %}
{% assign main_content = content_parts | last %}

{{ main_content | markdownify }}

<!-- <div class="posts">
  {% for post in paginator.posts %}
  <article class="post">
    <h1 class="post-title">
      <a href="{{ post.url | relative_url }}">
        {{ post.title }}
      </a>
    </h1>

    <time datetime="{{ post.date | date_to_xmlschema }}" class="post-date"
      >{{ post.date | date_to_string }}</time
    >

    {{ post.content }}
  </article>
  {% endfor %}
</div> -->

<!-- <div class="pagination">
  {% if paginator.next_page %}
  <a
    class="pagination-item older"
    href="{{ paginator.next_page_path | relative_url }}"
    >Older</a
  >
  {% else %}
  <span class="pagination-item older">Older</span>
  {% endif %} {% if paginator.previous_page %}
  <a
    class="pagination-item newer"
    href="{{ paginator.previous_page_path | relative_url }}"
    >Newer</a
  >
  {% else %}
  <span class="pagination-item newer">Newer</span>
  {% endif %}
</div> -->
