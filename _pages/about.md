---
permalink: /about/
title: "Contributors of the SliceFL project"
toc: true
toc_label: "Content"
toc_icon: "cog"
toc_sticky: true

---

## Introduction

The SliceFL project was created and is maintained by the Software Testing Group of the Department of Software Development at the University of Szeged, Institute of Informatics. Its research interests include testing, debugging and investigating the effectiveness of automatic debugging methods.

## The team

{% for team_member in site.team_members %}
  <img src="{{team_member.avatar}}" width="100" height="100"/>
  <a href="{{team_member.links.url}}">{{ team_member.name }}</a> - {{ team_member.position }}
  <hr>
{% endfor %}

## Contact us!

If you interested in any of our topics or just have a question, please contact us on <a href="mailto:slicefl@inf.u-szeged.hu">slicefl@inf.u-szeged.hu</a>
