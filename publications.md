---
layout: resume
title: List of Publications
---

<i class="ai ai-fw ai-google-scholar"></i> [View on Google Scholar](https://scholar.google.co.uk/citations?user=aPd4T_YAAAAJ)

Jump to: [[Articles](#articles)] [[Posters](#posters)] [[Theses](#theses)]

----

## Articles

{% for pub in site.data.cv.publications %}
{{pub.authors}}. **{{pub.title}}**. {% if pub.type == "conference" %} In *{{pub.journal}}*, pages {{pub.pages}}, {{pub.location}}, {{pub.date}}. {{pub.publisher}}. {% else %} *{{pub.journal}}* {% endif %} {% if pub.url %}[[link]({{pub.url}})]{% endif %}
{% endfor %}

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