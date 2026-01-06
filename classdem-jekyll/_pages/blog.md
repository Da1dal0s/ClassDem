---
layout: page
title: News & Events
subtitle: Latest updates from the ClassDem project.
permalink: /blog/
---

<ul class="post-list">
{% for post in site.posts %}
<li class="post-item">
    <div class="post-meta">
        <span class="category">{{ post.category }}</span> · {{ post.date | date: "%B %d, %Y" }}
    </div>
    <h3 class="post-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p class="post-excerpt">{{ post.excerpt | strip_html | truncate: 200 }}</p>
</li>
{% endfor %}
</ul>

{% if site.posts.size == 0 %}
<p>No posts yet. Check back soon for news and updates from the ClassDem project.</p>
{% endif %}
