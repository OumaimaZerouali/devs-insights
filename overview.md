---
layout: default
title: Overview
permalink: /overview
---
<hr />
<div class="dev-insight">
  <h3>I'm ready! I'm ready! I'm ready! ...to deploy to production!</h3>
  <p>
    Here you can find a overview of every blogpost I posted. Have fun!
  </p>
</div>
<hr />

<div class="main-content">
    <ul class="overview-posts" id="overview-content">
      {% for post in site.posts %}
        <li>
          <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
          <p class="post-meta">
            {{ post.date | date: "%B %d, %Y" }} - {{
            post.content | number_of_words }} words - {{
            post.content | number_of_words | divided_by: 200 }} min read
          </p>
        </li>
      {% endfor %}
    </ul>
</div>