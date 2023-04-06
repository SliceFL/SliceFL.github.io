---
permalink: /about/
title: "Contributors"
toc: true
toc_label: "Content"
toc_icon: "cog"
toc_sticky: true
header:
  overlay_image: /assets/images/banners/aboutus.jpg

---

## Introduction

The SliceFL project was initiated and is maintained by the Software Testing and Debugging Group of the Department of Software Engineering at the University of Szeged. Our research interests include testing, debugging, and investigating the effectiveness of automatic debugging methods.

## The team

{% for member in site.data.team.members %}
  <img src="{{member.avatar}}" width="100" height="100"/>
  <a href="{{member.webpage}}">{{ member.name }}</a> - {{ member.position }}
  <hr>
{% endfor %}

## Contact us!

If you are interested in any of our topics or just have a question, please contact us at <a href="mailto:slicefl@inf.u-szeged.hu">slicefl@inf.u-szeged.hu</a>

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/banners/aboutus_foot.png" alt="Here we are!">