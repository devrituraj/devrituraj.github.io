---
layout: page
permalink: /
title: about
nav: about
<!-- description: This is the personal website of Rituraj Singh -->

---
---

<div class="col p-0 pt-4 pb-4">
  <h1 class="pb-3 title text-left font-weight-bold">Rituraj Singh</h1>
  <h6 class="m-0 mb-2" style="font-size: 0.83em;">{{ page.description }}</h6>
  {% if page.address %}
      <h6 class="m-0 mb-2" style="font-size: 0.83em;">{{ page.address }}</h6>
  {% endif %}
</div>

<!-- Introduction -->

<div style="display: flex; flex-wrap: wrap;">
    <div class="text-justify p-0">
        <div class="col-xs-12 col-sm-6 p-0 pt-2 pb-sm-2 pb-4 pl-sm-4 text-center" style="float: right;">
          <img class="profile-img img-responsive" src="{{ 'prof_pic.jpg' | prepend: '/assets/img/' | prepend: site.baseurl | prepend: site.url }}">
        </div>

        <p>
            I was a PhD student at <a href="https://www.inria.fr/en" target="_blank">INRIA</a>, <a href="http://www.irisa.fr/en" target="_blank">IRISA</a> research center at Rennes, France. My thesis is entiled as "Data Centric Workflows for Crowdsourcing Applications", co-advised by <a href="http://people.rennes.inria.fr/Loic.Helouet/" target="_blank"> Dr. Loic Helouet</a> and <a href="http://people.irisa.fr/Zoltan.Miklos/" target="_blank">Dr. Zoltan Mikols</a>.
            I was a member of <a href="https://www-druid.irisa.fr/" target="_blank">DRUID</a> and <a href="http://www.irisa.fr/sumo/" target="_blank">SUMO</a> team.
        </p>

        <p>
            My PhD research focus was on developing algorithms for crowdsourcing applications, to propose formal model for complex workflows for crowdsourcing and developing human-in-loop algorithms by applying probabilistic based techniques and latent variable models.
            I am also passionate about applying machine learning methods in other doamains as healthcare, natural language processing, etc.
            Previously, I did some work in anamoly detection on sensor data and on detection of diseases based on data obtained using wearables. My area of interest are Data Centric Systems and Workflows, Machine Learning, Crowdsourcing, Probabilistic Modelling of Systems and Data Mining.
        </p>
    </div>
</div>

<div class="col text-justify p-0">
<p>
    Before I joined my PhD, I was working as a Researcher at <a href="https://www.tcs.com/research-and-innovation" target="_blank">Tata Consultancy Services (TCS) Research & Innovation Lab</a>, Kolkata, India. I worked on various data analytics problems, particularly related to healthcare and signals and applied machine learning techniques. I graduated from the Computer Science department of <a href="https://www.iitp.ac.in/index.php/en-us/" target="_blank">IIT Patna</a> in June, 2015. During my masters, I wrote my master thesis under supervision of <a href="http://www.iitg.ac.in/ashok/in" target="_blank">Dr. Ashok Singh Sairam</a> entitled "Push based User Selection in Crowdsensing".
</p>
</div>

<!-- News -->
<div class="news mt-3 p-0">
  <h1 class="title mb-4 p-0">news</h1>
  {% assign news = site.news | reverse %}
  {% for item in news limit: site.news_limit %}
    <div class="row p-0">
      <div class="col-sm-2 p-0">
        <span class="badge light-green darken-1 font-weight-bold text-uppercase align-middle date ml-3">
          {{ item.date | date: "%b %-d, %Y" }}
        </span>
      </div>
      <div class="col-sm-10 mt-2 mt-sm-0 ml-3 ml-md-0 p-0 font-weight-light text">
        <p>{{ item.content | remove: '<p>' | remove: '</p>' | emojify }}</p>
      </div>
    </div>
  {% endfor %}
</div>
