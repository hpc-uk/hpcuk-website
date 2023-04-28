---
layout: section
title: HPC Courses
summary: All the training opportunities available from UK HPC centres
banner: web_banners_02.jpg
---




<p>&nbsp;</p>


{% for course in site.courses %}
<div class="course-area">
  <a href="{{ course.url | prepend: site.baseurl }}" class="coursehead">{{ course.title }}</a> &nbsp; &nbsp; &nbsp;
  {{ course.tier2 }}

  <p class="course-date">

    {{ course.start_date | date_to_string }} 


	{% assign ed = course.end_date | date: "%Y%m%d" %}
	{% assign sd = course.start_date | date: "%Y%m%d" %}
	
	{% if ed > sd %}      <!-- Don't show end date if same as start date -->
	    - {{ course.end_date | date_to_string }}
	{% endif %}

  </p>  
        


  <p>
    {{ course.content | strip_html | truncatewords: 50 }}
  </p>


  <p>
    <hr/>
  </p>
</div>
{% endfor %}




