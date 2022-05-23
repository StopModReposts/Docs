# JSON Request

{% swagger method="get" path="/{game}/sites.json" baseUrl="https://api.stopmodreposts.org" summary="JavaScript Object Notation (JSON) Request" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="game" type="String" %}
e.g. "minecraft"
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
[
    {
        "domain": "example.com",
        "notes": "Malware alert!",
        "path": "/",
        "reason": "Illegal redistribution"
    },
    ...
]
```
{% endswagger-response %}
{% endswagger %}
