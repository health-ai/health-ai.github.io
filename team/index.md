---
title: Team
layout: page
coreteam:
- name: Łukasz Kidziński, Ph.D.
  task: Bioengineering postdoc
  image: https://avatars2.githubusercontent.com/u/981858?s=460&v=4
  link: http://kidzinski.com/
- name: Olga Afanasiev, MD, Ph.D
  task: Dermatology resident
  image: https://cap.stanford.edu/profiles/viewImage?profileId=155674&type=square&ts=1509532227672
  link: https://www.linkedin.com/in/olgafan/
- name: Joshua Tanner, Ph.D.
  task: MD Candidate
  image: https://media.licdn.com/dms/image/C4E03AQHsspo6jDwhSA/profile-displayphoto-shrink_800_800/0?e=1552521600&v=beta&t=xkdVo3tXRw-D9o4ThjQCg9lpItoWmBIeHu61yeEZstI
  link: https://www.linkedin.com/in/joshua-tanner-980071a6/
- name: Eric William Loreaux
  task: MS student bioengineering
  image: https://media.licdn.com/dms/image/C4E03AQGWMf73d4WeyA/profile-displayphoto-shrink_800_800/0?e=1552521600&v=beta&t=KGS903TiM2WCRI_zYG80U0WJbjJ5HN8zPT2SAdwmfhs
  link: https://www.linkedin.com/in/eric-loreaux-011672b2/
- name: Roxana Daneshjou
  task: Dermatology resident
  image: https://pbs.twimg.com/profile_images/786606324603695104/WWnvq1qu_400x400.jpg
  link: https://twitter.com/RoxanaDaneshjou?ref_src=twsrc%5Egoogle%7Ctwcamp%5Eserp%7Ctwgr%5Eauthor
- name: Milad Mohammadi, Ph.D.
  task: Data scientist
  image: https://pbs.twimg.com/profile_images/500003877400231937/Y1SPz9in.jpeg
  link: https://www.linkedin.com/in/milad-mohammadi-32999715/
- name: Mika Tabata
  task: MD Candidate
  image: https://s3.amazonaws.com/health-ai/website/images/people/mika.tabata.jpg
  link: https://www.linkedin.com/in/mika-tabata-61994027/
- name: Varun Vasudevan
  task: Ph.D. student 
  link: https://profiles.stanford.edu/varun-vasudevan
  image: https://profiles.stanford.edu/proxy/api/cap/profiles/81989/resources/profilephoto/350x350.1509500124813.jpg
- name: Masoud Badiei
  task: Postdoctoral Research Fellow 
  image: https://i1.rgstatic.net/ii/profile.image/584364404514816-1516334739737_Q512/Masoud_Badiei_Khuzani.jpg
  link: https://www.linkedin.com/in/masoud-badiei-khuzani-08a70a86/
- name: Hongyi Ren
  task: Research Data Analyst
  link: https://med.stanford.edu/profiles/hongyi-ren
  image: https://med.stanford.edu/profiles/images/profile-large-blank.png
advisors:
- name: Scott Delp, Ph.D.
  task: Bioengineering professor
  image: https://cap.stanford.edu/profiles/viewImage?profileId=6284&type=square&ts=1509499392349
  link: http://nmbl.stanford.edu/people/scott-delp/
- name: Lei Xing, Ph.D.
  task: Medical physics professor
  image: https://v2media-711f.kxcdn.com/wp-content/uploads/1900/12/Lei-Xing.jpg
  link: http://med.stanford.edu/xinglab.html
- name: Justin Ko, MD, MBA
  task: Chief Medical Dermatology
  image: https://cap.stanford.edu/profiles/viewImage?profileId=36790&type=square&ts=1509507671908
  link: https://profiles.stanford.edu/justin-ko
- name: Robert Chang, MD, MBA
  task: Assistant Professor of Ophthalmology
  image: https://cap.stanford.edu/profiles/viewImage?profileId=13794&type=square&ts=1509536853243
  link: https://profiles.stanford.edu/robert-chang
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
<div class="col s12 m4 center" style="margin-bottom: 1em;">
{% if person.github %}
<a href="https://github.com/{{ person.github }}" class="post-author">
   {{ person.name }}
</a>
{% else %}
<a href="{{ person.link }}" class="post-author">
<img src="{{ person.image }}" class="avatar" style="width: 70%;" /><br />
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
<div class="col s12 m4 center" style="margin-bottom: 1em;">
{% if person.github %}
<a href="https://github.com/{{ person.github }}" class="post-author">
   {{ person.name }}
</a>
{% else %}
<a href="{{ person.link }}" class="post-author">
<img src="{{ person.image }}" class="avatar" style="width: 70%;" /><br />
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
