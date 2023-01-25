---
layout: splash
permalink: /nyuszika/
title: "Welcome to my new site!"
date: 2020-09-14 14:37:43 +0300
author_profile: true
---
<!--default.html-->

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>{{page.title}}</title>
</head>
<body>
	# Nyuszika!
	
	
<ul>
    {% for post in site.posts %}
        <li><a href="{{ post.url | relative_url }}">{{post.title}}</a></li>
    {% endfor %}
</ul>
</body>
</html>