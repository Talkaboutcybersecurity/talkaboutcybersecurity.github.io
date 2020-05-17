---
layout: page
title: Archives
permalink: /archives/
sidebar_link: true
---
{% assign rawtags = "" %}
{% for post in site.posts %}
	{% assign ttags = post.tags | join:'|' | append:'|' %}
	{% assign rawtags = rawtags | append:ttags %}
{% endfor %}
{% assign rawtags = rawtags | split:'|' | sort %}

{% assign tags = "" %}
{% for tag in rawtags %}
	{% if tag != "" %}
		{% if tags == "" %}
			{% assign tags = tag | split:'|' %}
		{% endif %}
		{% unless tags contains tag %}
			{% assign tags = tags | join:'|' | append:'|' | append:tag | split:'|' %}
		{% endunless %}
	{% endif %}
{% endfor %}

<form name="category_form">
  <div class="radio-group">
  <input type="radio" id="option-one" name="selector" checked><label for="option-one">Category</label><input type="radio" id="option-two" name="selector">
  </div>
 </form>

<div id="ordered_by_categories" markdown="1">

{% for tag in tags %}
## {{ tag }}
	{% for post in site.posts %}
        {% for post_tag in post.tags %}
            {% if post_tag == tag %}
{{ post.date | date_to_string }} &raquo; [ {{ post.title }} ]({{ post.url }})
            {% break %}
            {% endif %}
        {% endfor %}
    {% endfor %}
{% endfor %}
</div>