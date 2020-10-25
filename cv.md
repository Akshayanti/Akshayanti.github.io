---
layout: resume
title: CV
---
## Current Occupation

Software Engineer (L1) at Twilio Czechia s.r.o, Prague, Czechia

## Education

`1990 - 1994`
__University Name__
Degree Awarded

`1995 - 1997`
__University Name__
Degree Awarded 

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
{{% if pub.type %}} {{pub.type}} under supervision of [{{pub.supervisor}}]({{pub.supervisor_link}})
{% if pub.supervisor2 %} and [{{pub.supervisor2}}]({{pub.supervisor2_link}}){% endif %}{{% endif %}}<br />
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


