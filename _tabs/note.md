---
layout: page
title: Note
icon: fas fa-pen-nib
order: 2
---

{% assign notes = site.categories['Note'] %}
{% if notes.size > 0 %}
{% for post in notes %}
<div style="margin-bottom: 2rem; padding-bottom: 1.5rem; border-bottom: 1px solid rgba(255,255,255,.06);">
  <a href="{{ post.url }}" style="font-size: 1.1rem; font-weight: 700; color: #e6edf3; text-decoration: none;">{{ post.title }}</a>
  <div style="font-size: .8rem; color: #8b949e; margin-top: .3rem;">{{ post.date | date: "%Y.%m.%d" }}</div>
  {% if post.excerpt %}
  <p style="font-size: .88rem; color: #8b949e; margin-top: .5rem; line-height: 1.6;">{{ post.excerpt | strip_html | truncate: 120 }}</p>
  {% endif %}
</div>
{% endfor %}
{% else %}
<p style="color: #8b949e;">아직 작성된 노트가 없습니다.</p>
{% endif %}
