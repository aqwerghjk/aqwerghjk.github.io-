---
layout: default
permalink: /목/
---
<script>
	window.onload=function(){document.getElementById("mthu").className="ctd"};
</script>
{% for page in site.pages %}
{% if page.categories contains 'thu' %}
<div class="img">
<a href="{{ page.url | prepend: site.baseurl }}">
<img src="{{ page.img }}" alt="{{ page.title }}">
<div id="img_text">{{ page.title }}
<div class="img_text">{% if page.num %}회차수: {{ page.num }}{% endif %}</div>
<div class="img_text">갱신일: {{ page.date | date: "%b %-d, %Y" }}</div></div>
</div></a>
</div>
{% endif %}
{% endfor %}