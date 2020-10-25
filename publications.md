---
layout: page
title: List of Publications
---

[Google Scholar](https://scholar.google.co.uk/citations?user=aPd4T_YAAAAJ)

Jump to: [Publications](#publications) [Theses](#theses)

## Publications

{% for pub in site.data.cv.publications %}
{{pub.author}}<br />
**{{pub.title}}**<br />
*{{pub.journal}}*
{% if pub.note %} *({{pub.note}})* {% endif %} *{{pub.month}}, {{pub.year}}*<br />
[[web]({% if pub.internal %}{{pub.url | prepend: site.url}}{% else %}{{pub.url}}{% endif %})]
{% if pub.doi %}[[doi]({{pub.doi}})]{% endif %}

{% endfor %}

## Theses

{% for pub in site.data.cv.theses %}
**{{pub.title}}**<br />
{{% if pub.type %}} {{pub.type}}. {{% endif %}} {% if pub.supervisor %} Supervised by *[{{pub.supervisor}}]({{pub.supervisor_link}})*. {% endif %} <br />
*{{pub.school}}*<br />
In *{{pub.month}}, {{pub.year}}* in *{{pub.address}}* <br />
{% if pub.url %}[[View Thesis]({{pub.url}})]{% endif %}

{% endfor %}