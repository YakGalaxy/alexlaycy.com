---
layout: page
title: Resources
id: resources
permalink: /resources/
categories:
collection:
excerpt: 
comments: false
---

# Guides

{% assign guides = site.guides | sort: 'title' %}
{% for guide in guides %}
- <a href="{{ guide.url | absolute_url }}" class="internal-link">{{ guide.title }}</a>
{% endfor %}

# Resources

{% assign resources = site.resources | sort: 'title' %}
{% for resource in resources %}
- <a href="{{ resource.url | absolute_url }}" class="internal-link">{{ resource.title }}</a>
{% endfor %}


