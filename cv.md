---
layout: resume
title: Curriculum Vitae 
---

<i class="fa fa-fw fa-github"></i> [Academic CV on Github](https://github.com/Akshayanti/myCV/blob/CVs/Resume_academic.pdf)  
<i class="fa fa-fw fa-github"></i> [Professional CV on Github](https://github.com/Akshayanti/myCV/blob/CVs/Resume_professional.pdf)

Jump to: <a href="#articles"><button>Articles</button></a> <a href="#posters"><button>Posters</button></a> <a href="#theses"><button>Theses</button></a>

----

## Professional Experience

{% for pub in site.data.cv.positions %}
`{{pub.date}}`
**{{pub.title}}** at **{{pub.company}}**, {{pub.location}}<br />
{% if pub.now_pos %} {{pub.now_pos}} `{{pub.now_pos_date}}`<br />{% endif %}
{% if pub.prev_pos %} {{pub.prev_pos}} `{{pub.prev_pos_date}}`<br />{% endif %}
{% if pub.task %} {{pub.task}} {% endif %}

{% endfor %}

## Education

{% for pub in site.data.cv.education %}
`{{pub.date}}`
**{{pub.title}}**, {{pub.affiliation}}, {{pub.location}}<br />
{% if pub.note %} *({{pub.note}})*<br />{% endif %}
{% if pub.thesis %} **Thesis Title:** {{pub.thesis}}<br /> {% endif %}
{% if pub.thesis %} **Supervisor(s):** {{pub.supervisor}} {% if pub.supervisor2 %} and {{pub.supervisor2}}{% endif %}{% 
endif %}

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

<!-- ### Footer

Last updated: Oct 25, 2020 -->


