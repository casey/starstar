## All about some humans
{% for person in people %}
{{person.name}} {{person.age}}, {{person.job}}
{% if person.allergies %}
*allergies:*
{% for allergy in person.allergies %}
- {{allergy}}
{% endfor %}
{% endif %}

{% endfor %}
## All about fruit
{% for fruit in fruits %}
The average {{fruit.name}} weighs {{fruit.weight}} and has {{fruit.calories}} calories.
{% endfor %}
