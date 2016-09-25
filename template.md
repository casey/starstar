## All about some humans
{% for person in people %}
{{person.name}}, {{person.age}}, {{person.job}}
{% endfor %}

## All about the days of the week
english | french | swedish
--- | --- | ---
{% for day in days %}
{{day.english}} | {{day.french}} | {{day.swedish}}
{% endfor %}
