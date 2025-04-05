---
layout: default
title: Overview
permalink: /overview/
---

<hr />
<div class="dev-insight">
  <h3>I'm ready! I'm ready! I'm ready! ...to deploy to production!</h3>
  <p>Here you can find an overview of every blog post I posted. Have fun!</p>
</div>
<hr />

<div class="main-content">
  <ul class="overview-posts" id="overview-content">
    {% for post in site.posts %}
    <li class="overview-post">
      <a href="{{ site.baseurl }}{{ post.url }}">
        {% if post.image %}
        <img
          src="{{ site.baseurl }}{{ post.image }}"
          alt="{{ post.title }}"
          class="overview-image"
        />
        {% endif %}
        <div class="overview-post-info">
          <h3>{{ post.title }}</h3>
          <p>{{ post.excerpt }}</p>
          <p class="post-meta">
            {{ post.date | date: "%B %d, %Y" }} - {{ post.content |
            number_of_words }} words - {{ post.content | number_of_words |
            divided_by: 200 }} min read
          </p>
        </div>
      </a>
    </li>
    {% endfor %}
  </ul>
</div>
