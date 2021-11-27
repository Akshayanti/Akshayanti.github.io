---
layout: resume
title: List of Publications
---

<i class="ai ai-fw ai-google-scholar"></i> [View on Google Scholar](https://scholar.google.co.uk/citations?user=aPd4T_YAAAAJ)

Jump to: [[Articles](#articles)] [[Posters](#posters)] [[Theses](#theses)]

----


## Articles

<ul>
    {% for pub in site.data.cv.publications %}
        <li>{{pub.authors}}.  {{pub.title}}.  {% if pub.type == "conference" %} In {{pub.journal}}, {% if pub.pages %}pages {{pub.pages}},{% endif %} {% if pub.volume %}volume {{pub.volume}} of {{pub.series}},{% endif %} {{pub.location}}, {{pub.date}}.  {{pub.publisher}}. {% else %} _{{pub.journal}}_, {{pub.volume}}({{pub.number}}):{{pub.pages}}, {{pub.year}}. ISSN {{pub.issn}}. {% endif %} {% if pub.url %}<a href="{{pub.url}}"><button>View Publication</button></a>{%endif %}</li><br />
    {% endfor %}
</ul>
----

## Posters

{% for pub in site.data.cv.posters %}
`{{pub.year}}`
{{pub.author}}<br />
**{{pub.title}}**<br />
*{{pub.conference}}, {{pub.venue}}*
<br />
[[View Poster]({% if pub.internal %}{{pub.url | prepend: site.url}}{% else %}{{pub.url}}{% endif %})]

{% endfor %}

----

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