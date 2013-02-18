---
layout: page
title: India High on JS
tagline: Internet of Things
---
{% include JB/setup %}

<div class="row">

  <div class="span8">
  	{% for post in site.posts %}
	  <h2><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h2>
	  <small><span>{{ post.date | date_to_string }}</span> written by <strong>Vishwas Sharma</strong></small>
	  <hr class="soften">
	  <p>{{ post.content }}</p>
	  <hr class="soften">
	{% endfor %}
  </div>

  <!-- Right side content -->
  <div class="span4">
	{% for tag in site.tags %} 
	  <h3 id="{{ tag[0] }}-ref">{{ tag[0] }}</h3>
	  <ul>
	    {% assign pages_list = tag[1] %}  
	    {% include JB/pages_list %}
	  </ul>
	{% endfor %}
  </div>
</div>

<!-- 
<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul> -->