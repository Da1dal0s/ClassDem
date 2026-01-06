---
layout: page
title: Events
permalink: /events/
---

## Upcoming Events

Stay tuned for upcoming lectures, workshops, and conferences related to the ClassDem project.

---

## Past Events

{% assign event_posts = site.posts | where: "category", "Event" %}
{% if event_posts.size > 0 %}
<ul class="post-list">
{% for post in event_posts %}
  <li class="post-item">
    <div class="post-meta">
      <span class="category">{{ post.category }}</span> · {{ post.date | date: "%B %d, %Y" }}
    </div>
    <h3 class="post-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p class="post-excerpt">{{ post.excerpt | strip_html | truncate: 200 }}</p>
  </li>
{% endfor %}
</ul>
{% else %}
<p>No past events to display yet. Check back soon for updates on our lectures, workshops, and conferences.</p>
{% endif %}
