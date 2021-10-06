---
layout: page
excerpt: "About Me..."
---

At present, I'm working as a software engineer with Twilio in Prague, Czechia.

Graduate of [LCT Program](https://lct-master.org/), I did my master's in Computational Linguistics from
Charles University (Czechia, 2021) and University of Basque Country (Spain, 2019). 

Whatever free time I find from work and reading, I devote to automating mundane tasks by scripting them, trying to learn and/or
read about different languages in the world, browsing random articles on wikipedia, and gaming.

## On Reading

I used to read more voraciously, but have recently lost my way with the books. A few works I have tremendously enjoyed
include {% for pub in site.data.books.books %} **{{pub.name}}** ({{pub.author}}), {% endfor %} among others.

Apart from those listed above already, some of my other favorite authors include {% for pub in site.data.books.authors %}
{{pub}}, {% endfor %} and Sarat Chandra Chattopadhyay.

If I had to recommend a few works that everyone would benefit from, I'd pick the following:
{% for pub in site.data.books.recommended %}
- **{{pub.name}}** by {{pub.author}}<br />
Originally written in {{pub.original}}<br />
[[More on this book]({{pub.goodreads}})]

{% endfor %}
 
## Research Interests

So far, I have been trying to better understand the concepts of {% for pub in site.data.cv.research_interests1 %} {{pub}}, 
{% endfor %} while focusing on Universal Dependencies Project.

I have been equally interested in {% for pub in site.data.cv.research_interests2 %} {{pub}}, {% endfor %} and am trying to
learn more about them, whilst trying to solve more and more problems related to Indic and low-resource languages.
