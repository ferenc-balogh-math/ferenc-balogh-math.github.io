{% for pub in site.data.publications %}

### {{ pub.title }}

**{{ pub.authors }}**  
*{{ pub.journal }}*{% if pub.volume %}, {{ pub.volume }}{% endif %} ({{ pub.year }}), {{ pub.pages }}

{% if pub.abstract %}
<details>
<summary>Abstract</summary>
{{ pub.abstract }}
</details>
{% endif %}

{% if pub.url %}[Link]({{ pub.url }}){% endif %}
{% if pub.pdf %} | [PDF]({{ pub.pdf }}){% endif %}
{% if pub.doi %} | DOI: {{ pub.doi }}{% endif %}

---

{% endfor %}
