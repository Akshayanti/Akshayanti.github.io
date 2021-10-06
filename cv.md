---
layout: resume
title: Curriculum Vitae 
---

<i class="fa fa-fw fa-github"></i> [Academic CV on Github](https://github.com/Akshayanti/myCV/blob/CVs/Resume_academic.pdf)  
<i class="fa fa-fw fa-github"></i> [Professional CV on Github](https://github.com/Akshayanti/myCV/blob/CVs/Resume_professional.pdf)

## Current Occupation

{{site.data.cv.position}} at {{site.data.cv.affiliation}}, {{ site.data.cv.address }}

**Quick Navigation Links**:<br />
[[Professional Experience](#professional-experience)] [[Education](#education)] <br />
[[Other Details](#other-details)] [[References](#references)]

----

## Professional Experience

{% for pub in site.data.cv.positions %}
`{{pub.date}}`
**{{pub.title}}** at **{{pub.company}}**, {{pub.location}}<br />
{{% if pub.now_pos %}} {{pub.now_pos}} `{{pub.now_pos_date}}` <br />{{% endif %}}
{{% if pub.prev_pos %}} {{pub.prev_pos}} `{{pub.prev_pos_date}}` <br />{{% endif %}}
{{% if pub.task %}} {{pub.task}} {{% endif %}}

{% endfor %}

## Education

{% for pub in site.data.cv.education %}
`{{pub.date}}`
**{{pub.title}}**, {{pub.affiliation}}, {{pub.location}}<br />
{% if pub.note %} *({{pub.note}})*<br />{% endif %}
{% if pub.thesis %} Thesis Title: {{pub.thesis}}<br /> {% endif %}
{% if pub.thesis %} Supervisor(s): {{pub.supervisor}} {% if pub.supervisor2 %} and {{pub.supervisor2}}{% endif %}{% endif %}

{% endfor %}

## Other Details

### Spoken Languages

{% for pub in site.data.cv.language %}
`{{pub.level}}`
{{pub.name}}

{% endfor %}

### Awards and Extra-Curriculars

{% for pub in site.data.cv.awards %}
`{{pub.year}}`
{{pub.detail}}

{% endfor %}

## References

{% for pub in site.data.cv.references %}
**{{pub.name}}**<br />
{{pub.affiliation}}<br />
<i class="fa fa-fw fa-envelope-square"></i> [{{pub.mail}}](mailto:{{pub.mail}})

{% endfor %}



<!-- ### Footer

Last updated: Oct 25, 2020 -->


