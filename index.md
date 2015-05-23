---
layout: default
---

**{{ site.conference.location }}**,
{% assign startdate = site.conference.dates | first %}
{% assign enddate = site.conference.dates | last %}
{% if startdate.month == enddate.month %}
{{ startdate.date }} - {{ enddate.date }} {{ startdate.month }} {{ startdate.year }}<br>
{% else %}
{{ startdate.date }} {{ startdate.month }} - {{ enddate.date }} {{ enddate.month }} {{ startdate.year }}
{% endif %}
{% if site.conference.hosturl %} [Hosts Local Page](https://sites.google.com/site/gpapprox/home)<br>{% endif %}
{% if site.conference.organizers %} organized by {% for person in site.conference.organizers %}[{{ person.name }}]({{ person.url }}){% if site.conference.organizers | size > 1 %}, {% endif %}{% endfor %}{% endif %}

{% if site.conference.hosts %}hosted by {% for person in site.conference.hosts %}[{{ person.name }}]({{ person.url }}){% if site.conference.hosts | size > 1 %}, {% endif %}{% endfor %}{% endif %}

{% for date in site.conference.dates %}
## {{ date.day }} {{ date.date }} {{ date.month }} 
{% for slot in site.data.lectures %}
{% assign thedate = slot.date | plus: 0%}
{% if date.date == thedate %}
{% if slot.start %}{{ slot.start }} {% if slot.end %}- {{ slot.end }} {% endif %}{% endif %}{% if slot.pdf %}[{{ slot.title }}]({{ slot.pdf }}){% else %}{{ slot.title }}{% endif %}{% if slot.speaker %}, {{ slot.speaker }}{% endif %}{% if slot.institution %}, {{ slot.institution }}{% endif %}{% if slot.ipynb %} [[jupyter notebook]({{ slot.ipynb }})]{% endif %}
{% if slot.youtube %}
<iframe width="{{ site.youtube.width }}" height="{{ site.youtube.height }}" src="https://www.youtube.com/embed/{{ slot.youtube }}" frameborder="0" allowfullscreen></iframe>
{% endif %}
{% endif %}
{% endfor %}
{% endfor %}

