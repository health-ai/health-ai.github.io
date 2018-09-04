---
layout: page
title: Team
coreteam:
  - github: kidzik
    name: Łukasz Kidziński
    task: Bioengineering postdoc
  - name: Olga Afanasiev
    task: Dermathology resident
    image: https://cap.stanford.edu/profiles/viewImage?profileId=155674&type=square&ts=1509532227672
    link: https://www.linkedin.com/in/olgafan/
  - name: Milad Mohammadi
    task: Data scientist
    image: https://pbs.twimg.com/profile_images/500003877400231937/Y1SPz9in.jpeg
    link: https://www.linkedin.com/in/milad-mohammadi-32999715/
advisors:
  - name: Scott Delp
    task: Bioengineering professor
    image: https://cap.stanford.edu/profiles/viewImage?profileId=6284&type=square&ts=1509499392349
    link: http://nmbl.stanford.edu/people/scott-delp/
  - name: Lei Xing
    task: Medical physics professor
    image: https://v2media-711f.kxcdn.com/wp-content/uploads/1900/12/Lei-Xing.jpg
    link: http://med.stanford.edu/xinglab.html
---
<style>
.person {
text-align: center
}
.person img {
margin: 0.3em;
}
.person span {
display: block;
padding-top: 0.3em;
font-size: 0.8em;
}
</style>
<div style="margin-top: 20px;" class="post-content">

<h1>Team</h1>
{% for person in page.coreteam %}
{% assign loopindex = forloop.index0 | modulo: 3 %}
{% if loopindex == 0 or forloop.first %}
<div class="row">
{% endif %}
<div class="col s4 center">
{% if person.github %}
<a href="https://github.com/{{ person.github }}" class="post-author">
   {% avatar user=person.github size=200 %}<br />
   {{ person.name }}
</a>
{% else %}
<a href="{{ person.link }}" class="post-author">
<img src="{{ person.image }}" class="avatar" style="width: 200px;" /><br />
   {{ person.name }}
</a>
{% endif %}
<span>{{ person.task }}</span>
</div>
{% if loopindex == 3 or forloop.last %}
</div>
{% endif %}
{% endfor %}

<h1>Advisors</h1>
{% for person in page.advisors %}
{% assign loopindex = forloop.index0 | modulo: 3 %}
{% if loopindex == 0 or forloop.first %}
<div class="row">
{% endif %}
<div class="col s4 center">
{% if person.github %}
<a href="https://github.com/{{ person.github }}" class="post-author">
   {% avatar user=person.github size=200 %}<br />
   {{ person.name }}
</a>
{% else %}
<a href="{{ person.link }}" class="post-author">
<img src="{{ person.image }}" class="avatar" style="width: 200px;" /><br />
   {{ person.name }}
</a>
{% endif %}
<span>{{ person.task }}</span>
</div>
{% if loopindex == 3 or forloop.last %}
</div>
{% endif %}
{% endfor %}



</div>
