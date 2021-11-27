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
        <li>{{pub.authors}}.  {{pub.title}}.  {% if pub.type == "conference" %} In <em>{{pub.journal}}</em>, {% if pub.pages %}pages {{pub.pages}},{% endif %} {% if pub.volume %}volume {{pub.volume}} of {{pub.series}},{% endif %} {{pub.location}}, {{pub.date}}.  {{pub.publisher}}. {% else %} <em>{{pub.journal}}</em>, {{pub.volume}}({{pub.number}}):{{pub.pages}}, {{pub.year}}. ISSN {{pub.issn}}. {% endif %} {% if pub.url %}<a href="{{pub.url}}"><button>View Publication</button></a>{%endif %}</li><br />
    {% endfor %}
</ul>
----

## Posters

<ul>
    {% for pub in site.data.cv.posters %}
        <li>{{pub.authors}}.  Poster: {{pub.title}}. In <em>{{pub.conference}}</em>, {{pub.venue}}, {{pub.year}}. {% if pub.url %}<a href="{% if pub.internal %}{{pub.url | prepend: site.url}}{% else %}{{pub.url}}{% endif %}"><button>View Poster</button></a>{%endif %}</li><br />
    {% endfor %}
</ul>
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