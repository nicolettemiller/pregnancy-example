---
title: "Involved"
layout: gridlay
sitemap: false
permalink: /involved/
---

## Get Involved

<div class="jumbotron">
  <h3>Avenues for Collaboration</h3>
  <strong>Submission:</strong> Idea for research? Please submit a brief paragraph with the following details: Investigator, email, institution, title, brief synopsis detailing proposed participants, data sources and analyses.

  <strong>Next steps:</strong> The advisory committee meets monthly to review these data requests, meet formally with submitting investigator to propose best strategy, and pool interested centers to expedite collaborations.
</div>

<br>

## Individuals

<div class='jumbotron'>
{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 4 %}

{% if even_odd == 0 %}

<div class="row">
{% endif %}

<div class="col-sm-3">
<img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" width="100%" style="max-width:250px"/>
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}<br></i>
</div>

<!-- {% if member.website %}<a href="{{ member.website }}" target="_blank"><i class="fa fa-home fa-2x"></i></a> {% endif %} -->
<!-- {% if member.email %}<a href="mailto:{{ member.email }}" target="_blank"><i class="fa fa-envelope-square fa-2x"></i></a> {% endif %} -->
<!-- {% if member.scholar %} <a href="{{ member.scholar }}" target="_blank"><i class="ai ai-google-scholar-square ai-2x"></i></a> {% endif %} -->
<!-- {% if member.cv %} <a href="{{ member.cv }}" target="_blank"><i class="ai ai-cv-square ai-2x"></i></a> {% endif %} -->
<!-- {% if member.github %} <a href="{{ member.github }}" target="_blank"><i class="fa fa-github-square fa-2x"></i></a> {% endif %} -->
<!-- {% if member.researchgate %} <a href="{{ member.researchgate }}" target="_blank"><i class="ai ai-researchgate-square ai-2x"></i></a> {% endif %} -->
<!-- </div> -->

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 3 %}

</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 4 %}
{% if even_odd != 0 %}

</div>
{% endif %}
</div>
