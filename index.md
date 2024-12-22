---
layout: default
title: "Home"
---

# Welcome to the Top 10 Posts Page

Here are the top 10 posts from our blog:

{% for post in site.posts limit:10 %}
  <article class="post">
    <h2><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>
    <p class="date">{{ post.date | date: "%B %d, %Y" }}</p>
    <div class="entry">
      {{ post.excerpt }}
    </div>
    <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
  </article>
{% endfor %}
