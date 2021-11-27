---
layout: resume
title: Curriculum Vitae 
---

<i class="fa fa-fw fa-github"></i> [Academic CV on Github](https://github.com/Akshayanti/myCV/blob/CVs/Resume_academic.pdf)  
<i class="fa fa-fw fa-github"></i> [Professional CV on Github](https://github.com/Akshayanti/myCV/blob/CVs/Resume_professional.pdf)

Jump to: <a href="#professional-experience"><button>Professional Experience</button></a> <a href="#education"><button>Education</button></a> <a href="#miscellaneous"><button>Miscellaneous</button></a> <a href="#references"><button>References</button></a>

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

## Miscellaneous

asd

### Languages

<ul>
    {% for pub in site.data.cv.language %}
        <li>{{pub.level}} fluency in {{pub.name}}</li>
    {% endfor %}
</ul>

### Awards and Extra-Curriculars

<ul>
    {% for pub in site.data.cv.awards %}
        <li>{{pub.year}}, {{pub.detail}}</li>
    {% endfor %}
</ul>

## References

{% for pub in site.data.cv.references %}
**{{pub.name}}**<br />
{{pub.affiliation}}<br />
<i class="fa fa-fw fa-envelope-square"></i> [{{pub.mail}}](mailto:{{pub.mail}})

{% endfor %}
