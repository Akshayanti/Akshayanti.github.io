---
layout: resume
title: CV
---

## Current Occupation

Software Engineer (L1) at Twilio Czechia s.r.o, Prague, Czechia

Quick Navigation: [[Education](#education)] [[Publications](#publications)] [[Theses](#theses)] [[Professional Experience](#professional-experience)] [[References](#references)]

----

## Education

{% for pub in site.data.cv.education %}
`{{pub.date}}`
**{{pub.title}}**, **{{pub.affiliation}}, {{pub.location}}**<br />
{% if pub.note %} *({{pub.note}})*<br />{% endif %}
{% if pub.thesis %} Thesis Title: {{pub.thesis}}<br /> {% endif %}
{% if pub.thesis %} Supervisor(s): {{pub.supervisor}} {% if pub.supervisor2 %} and {{pub.supervisor2}}{% endif %}{% endif %}

{% endfor %}

## Publications

{% for pub in site.data.cv.publications %}
`{{pub.year}}`
{{pub.author}}<br />
**{{pub.title}}**<br />
*{{pub.journal}}*
{% if pub.note %} *({{pub.note}})* {% endif %}<br />
[[web]({% if pub.internal %}{{pub.url | prepend: site.url}}{% else %}{{pub.url}}{% endif %})]
{% if pub.doi %}[[doi]({{pub.doi}})]{% endif %}

{% endfor %}

## Theses

{% for pub in site.data.cv.theses %}
`{{pub.year}}`
**{{pub.title}}**<br />
{{% if pub.type %}} {{pub.type}}. Supervised by [{{pub.supervisor}}]({{pub.supervisor_link}})
{% if pub.supervisor2 %} and [{{pub.supervisor2}}]({{pub.supervisor2_link}}){% endif %}.{{% endif %}}<br />
*{{pub.school}}*<br />
In *{{pub.address}}* <br />
{% if pub.url %}[[View Thesis]({{pub.url}})]{% endif %}

{% endfor %}

## Professional Experience

`Nov 2020 - Present`
__Software Engineer (L1)__, Twilio Czechia s.r.o
Prague, Czechia  

`April - October 2020`
__Intern Software Engineer (L1)__, Twilio Czechia s.r.o 

- Task
- Task

## References

{% for pub in site.data.cv.references %}
**{{pub.name}}**<br />
{{pub.affiliation}}<br />
Email: [{{pub.mail}}](mailto:{{pub.mail}})

{% endfor %}



<!-- ### Footer

Last updated: Oct 25, 2020 -->


