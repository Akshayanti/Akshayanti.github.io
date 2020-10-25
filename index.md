---
layout: page
excerpt: "About Me..."
---

Currently working as a software engineer, I recently finished my master's degree from Charles University, Prague.

I used to read more voraciously, but have recently lost my way with the books. A few works I have tremendously enjoyed are

{% for pub in site.data.books.books %}
- {{pub.name}} ({{pub.author}})

{% endfor %}

Apart from those listed above already, some of my other favorite authors include

{% for pub in site.data.books.authors %}
- {{pub}}

{% endfor %}

If I had to recommend a few works that everyone would benefit from, I'd pick the following:

{% for pub in site.data.books.recommended %}
- **{{pub.name}}** by {{pub.author}}<br />
Originally written in {{pub.original}}<br />
[[This book on goodreads]({{pub.goodreads}})]

{% endfor %}
 
## Research Interests

{% for pub in site.data.cv.research_interests %}
- {{pub}}
{% endfor %}
