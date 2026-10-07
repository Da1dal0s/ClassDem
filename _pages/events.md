---
layout: page
title: Events
permalink: /events/
---

## Upcoming Events

{% assign event_posts = site.posts | where: "category", "Event" %}
{% assign today = "now" | date: "%s" %}
{% assign upcoming_events = "" | split: "" %}
{% for post in event_posts %}
  {% assign post_date = post.date | date: "%s" %}
  {% if post_date >= today %}
    {% assign upcoming_events = upcoming_events | push: post %}
  {% endif %}
{% endfor %}

{% if upcoming_events.size > 0 %}
<ul class="post-list">
{% for post in upcoming_events %}
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
<p>Stay tuned for upcoming lectures, workshops, and conferences related to the ClassDem project.</p>
{% endif %}

---

## Past Events

{% assign past_events = "" | split: "" %}
{% for post in event_posts %}
  {% assign post_date = post.date | date: "%s" %}
  {% if post_date < today %}
    {% assign past_events = past_events | push: post %}
  {% endif %}
{% endfor %}

{% if past_events.size > 0 %}
<ul class="post-list">
{% for post in past_events %}
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
