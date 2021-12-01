---
layout: page
permalink: /misc/seminar/
title: Early Career Faculty Mentorship Program and Friday Research/Teaching Seminar Series
description: 
semesters: [Fall 2021 Schedule]
nav: false
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0" align="center">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/school_of_business.jpg' | relative_url }}" alt="" title="example image" style="width:600px;height:400px;"/>
        <img class="img-fluid" src="{{ '/assets/img/slu_logo.png' | relative_url }}" alt="" title="example image" style="width:280px;height:100px;position:absolute;top:25px;left:120px;"/>
    </div>
</div>

<br>

The Friday Research/Teaching seminar series is intended to bring together business school faculty, doctoral students, and faculty from neighboring institutions in interdisciplinary groups for the purpose of developing new areas of research and teaching through sustained intellectual collaboration. 

The seminar series also features the [Early Career Faculty Mentorship Program](/assets/misc/2021-mentor-program.pdf){:target="\_blank"} chaired by Dr. [Jintong Tang](https://www.slu.edu/business/about/faculty/tang-jintong.php){:target="\_blank"}. The goal is to "provide orientation, guidance, mentoring, and inclusive developmental practices" for early career faculty by strengthening peer-engagement among early career colleagues; creating a framework for mentorship by experienced colleagues within and across departments; providing an opportunity for early career teachers and scholars to engage with more experienced academics for mutually fruitful interactions; and facilitating the development of knowledge- and experience-sharing, caring, and FUN environment.
* **Time:** Fridays 12:00pm-1:00pm
* **Location:** Cook Hall Room L30

<div class="publications">

{% for y in page.semesters %}
  <h2 class="topic">{{y}}</h2>
  
  {% bibliography -f schedule -q @*[semester={{y}}]* %}
{% endfor %}

<h2 class="topic">Seminar Participants</h2>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/seminar/Oct1-21-1.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/seminar/Oct1-21-2.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/seminar/Oct1-21-3.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    Becoming a dedicated and effective teacher, 10/01/2021.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/seminar/Oct8-21-1.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/seminar/Oct8-21-2.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/seminar/Oct8-21-3.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    Mentorship program kickoff meeting, 10/08/2021.
</div>

</div>
