---
layout: page
title: 
tagline: Supporting tagline
---
{% include JB/setup %}

<div class="jenny_main">
	<ul class="posts">
	  {% for post in site.posts %}
	    <li class="jenny_postlist">
	    	<div class="title">
	    		<a  href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a>
	    	</div>
	    	<div class="time">{{ post.date | date: "%F"  }}</div>

	    	<div class="jenny_post_show"><div class="jenny_post_show_content">{{ post.content }}</div></div>
	    	<div class="jenny_all">......<div>
	    </li>
	  {% endfor %}
	</ul>
</div>


