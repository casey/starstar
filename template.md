## All about some humans
{% for person in people %}
- {{person.name}}, {{person.age}}, is a {{person.job}}{% if person.pets %} and has {{person.pets | length}} {{ 'pet' if (person.pets | length) == 1 else 'pets' }}:
{% for pet in person.pets %}
  - {{pet.name}}, a cute little {{pet.species}} who is {{pet.age}} years old and likes {{pet.likes}}
{% endfor %}
{% endif %}


{% endfor %}

## All about the days of the week
english | french | swedish
--- | --- | ---
{% for day in days %}
{{day.english}} | {{day.french}} | {{day.swedish}}
{% endfor %}
