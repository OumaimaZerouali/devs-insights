---
layout: default
---

<hr />
<div class="dev-insight">
  <h3>I'm ready! I'm ready! I'm ready! ...to deploy to production!</h3>
  <p>
    Welcome to my blog! Here, I share my insights on IT, programming, and the
    joys and challenges of working in development teams. Expect to find
    articles on coding techniques, project management, and the occasional
    anecdote from the trenches of software development.
  </p>
</div>
<hr />

<div class="main-content">
  <div class="featured-post">
    {% assign featured_post = site.posts.first %}
    {% if featured_post %}
    <a href="{{ featured_post.url | relative_url }}">
      {% if featured_post.image %}
      <img
        src="{{ featured_post.image }}"
        alt="{{ featured_post.title }}"
      />
      {% endif %}
      <p class="post-meta">
        {{ featured_post.date | date: "%B %d, %Y" }} - {{
        featured_post.content | number_of_words }} words - {{
        featured_post.content | number_of_words | divided_by: 200 }} min read
      </p>
      <h2>{{ featured_post.title }}</h2>
      <p>{{ featured_post.excerpt }}</p>
    </a>
    {% endif %}
  </div>

  <div class="sidebar-posts">
    {% assign sidebar_posts = site.posts | slice: 1, 5 %}
    {% for post in sidebar_posts %}
    <div class="sidebar-post">
      <a href="{{ post.url | relative_url }}">
        {% if post.image %}
        <img
          src="{{ post.image }}"
          alt="{{ post.title }}"
          class="sidebar-image"
        />
        {% endif %}
        <div class="sidebar-post-info">
          <h3>{{ post.title }}</h3>
          <p class="post-meta">
            {{ post.date | date: "%B %d, %Y" }} - {{
            post.content | number_of_words }} words - {{
            post.content | number_of_words | divided_by: 200 }} min read
          </p>
        </div>
      </a>
    </div>
    {% endfor %}
    {% if site.posts.size > 6 %}
        <div class="more-posts">
          <a href="{{ site.baseurl }}/overview" class="button">More Posts</a>
        </div>
    {% endif %}
  </div>
</div>


