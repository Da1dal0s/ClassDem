---
layout: page
title: Our Team
subtitle: The scholars and researchers driving the ClassDem project at the University of Edinburgh.
permalink: /team/
---

## Principal Investigator

{% for member in site.data.team.core %}
{% if member.role == "Principal Investigator" %}
<div style="display: grid; grid-template-columns: 200px 1fr; gap: 2rem; margin-bottom: 3rem; background: white; padding: 2rem; border-radius: 8px;">
<div style="text-align: center;">
<div style="width: 150px; height: 150px; border-radius: 50%; background: var(--marble-gray); display: flex; align-items: center; justify-content: center; font-family: 'Cinzel', serif; font-size: 3rem; color: var(--text-secondary); margin: 0 auto; overflow: hidden; border: 3px solid var(--bronze);">
{% if member.image %}
<img src="{{ member.image | relative_url }}" alt="{{ member.name }}" style="width: 100%; height: 100%; object-fit: cover;">
{% else %}
{{ member.initials }}
{% endif %}
</div>
</div>
<div>
<h3 style="margin-top: 0;">{{ member.name }}</h3>
<p><strong style="color: var(--bronze);">{{ member.role }}</strong><br>
{{ member.position }}, {{ member.affiliation }}</p>
<p>{{ member.bio }}</p>
<p><a href="mailto:{{ member.email }}">{{ member.email }}</a> · <a href="{{ member.url }}" target="_blank" rel="noopener noreferrer">Edinburgh Profile →</a></p>
</div>
</div>
{% endif %}
{% endfor %}

## Core Team

<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 2rem;">
{% for member in site.data.team.core %}
{% unless member.role == "Principal Investigator" %}
<div style="background: white; padding: 1.5rem; border-radius: 8px; text-align: center;">
<div style="width: 120px; height: 120px; border-radius: 50%; background: var(--marble-gray); display: flex; align-items: center; justify-content: center; font-family: 'Cinzel', serif; font-size: 2rem; color: var(--text-secondary); margin: 0 auto 1rem; overflow: hidden; border: 3px solid var(--bronze);">
{% if member.image %}
<img src="{{ member.image | relative_url }}" alt="{{ member.name }}" style="width: 100%; height: 100%; object-fit: cover;">
{% else %}
{{ member.initials }}
{% endif %}
</div>
<h4>{{ member.name }}</h4>
<p><strong style="color: var(--bronze);">{{ member.role }}</strong><br>
{{ member.position }}</p>
<p style="font-size: 0.95rem;">{{ member.bio }}</p>
{% if member.url %}<p><a href="{{ member.url }}" target="_blank" rel="noopener noreferrer">Profile →</a></p>{% endif %}
</div>
{% endunless %}
{% endfor %}
</div>

## Postdoctoral Fellows

<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 2rem;">
{% for member in site.data.team.postdocs %}
<div style="background: white; padding: 1.5rem; border-radius: 8px;">
<h4>{{ member.name }}</h4>
<p><strong style="color: var(--terracotta);">{{ member.role }}</strong><br>
{{ member.position }}</p>
<p style="font-size: 0.95rem;">{{ member.bio }}</p>
{% if member.url %}<p><a href="{{ member.url }}" target="_blank" rel="noopener noreferrer">Profile →</a></p>{% endif %}
</div>
{% endfor %}
</div>

## PhD Students

<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 2rem;">
{% for member in site.data.team.phd_students %}
<div style="background: white; padding: 1.5rem; border-radius: 8px;">
<h4>{{ member.name }}</h4>
<p><strong style="color: var(--terracotta);">{{ member.role }}</strong><br>
{{ member.position }}</p>
<p style="font-size: 0.95rem;">{{ member.bio }}</p>
</div>
{% endfor %}
</div>

## Project Administration

<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 2rem;">
{% for member in site.data.team.admin %}
<div style="background: white; padding: 1.5rem; border-radius: 8px;">
<h4>{{ member.name }}</h4>
<p><strong style="color: var(--terracotta);">{{ member.role }}</strong><br>
{{ member.position }}</p>
<p style="font-size: 0.95rem;">{{ member.bio }}</p>
</div>
{% endfor %}
</div>

## Affiliated Team Members

<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 2rem;">
{% for member in site.data.team.affiliated %}
<div style="background: white; padding: 1.5rem; border-radius: 8px;">
<h4>{{ member.name }}</h4>
<p><strong style="color: var(--terracotta);">{{ member.role }}</strong></p>
</div>
{% endfor %}
</div>
