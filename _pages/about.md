---
permalink: /about/
title: "Contributors of the SliceFL project"
toc: true
toc_label: "Content"
toc_icon: "cog"
toc_sticky: true

---


## The team

{% for team_member in site.team_members %}
  <img src="{{team_member.avatar}}" width="100" height="100"/>
  <a href="{{team_member.links.url}}">{{ team_member.name }}</a> - {{ team_member.position }}
  <p><em>Quote: </em>{{ team_member.content | markdownify }}</p>
  <hr>
{% endfor %}


