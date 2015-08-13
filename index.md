---
layout: page
title: 
tagline: Supporting tagline
---
{% include JB/setup %}

<div class="jenny_main clearfix">
	<div class="sidebar">
		<div>
			<!-- <div class="title">标签</div> -->
			<div class="title">
				<ul class="tag_box inline">
				  {% assign tags_list = site.tags %}  
				  {% include JB/tags_list %}
				</ul>


				{% for tag in site.tags %} 
				  <h2 id="{{ tag[0] }}-ref">{{ tag[0] }}</h2>
				  <ul>
				    {% assign pages_list = tag[1] %}  
				    {% include JB/pages_list %}
				  </ul>
				{% endfor %}

			</div>
		</div>
    </div>
    <div style="width:70%;">
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

</div>



