---
layout: resume
title: List of Publications
---

<i class="ai ai-fw ai-google-scholar"></i> [Google Scholar Page](https://scholar.google.co.uk/citations?user=aPd4T_YAAAAJ)

Jump to: <a href="#articles"><button>Articles</button></a> <a href="#posters"><button>Posters</button></a> <a href="#theses"><button>Theses</button></a>

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

<ul>
    {% for pub in site.data.cv.theses %}
        <li>Akshay Aggarwal.  {{pub.title}}.  {{pub.type}} thesis. {{pub.school}}, {{pub.address}}, {{pub.year}}. Thesis Supervisor {{pub.supervisor}}. {% if pub.url %}<a href="{% if pub.internal %}{{pub.url | prepend: site.url}}{% else %}{{pub.url}}{% endif %}"><button>View Thesis</button></a>{%endif %}</li><br />
    {% endfor %}
</ul>