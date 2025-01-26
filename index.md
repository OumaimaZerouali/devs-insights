---
layout: default
---

{% for post in site.posts %}
  <article class="post">
    {% if post.image %}
      <div class="post-image">
        <img src="{{ post.image }}" alt="">
        <div class="post-overlay">
          <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
          <p class="post-meta">{{ post.date | date: "%B %d, %Y" }}</p>
        </div>
      </div>
    {% endif %}
  </article>
{% endfor %}

<div class="pagination">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path | relative_url }}">Previous</a>
  {% endif %}

  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path | relative_url }}">Next</a>
  {% endif %}
</div>
