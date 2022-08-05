{% for tag in include.list.tags %}
    • <a href="/tag/{{ tag }}">{{ tag }}</a>
{% endfor %}