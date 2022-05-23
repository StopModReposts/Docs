# Requests

{% swagger method="get" path="/{game}/sites.json" baseUrl="https://api.stopmodreposts.org" summary="JavaScript Object Notation (JSON)" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="game" type="String" %}
e.g. "minecraft" (optional)
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

{% swagger method="get" path="/{game}/sites.xml" baseUrl="https://api.stopmodreposts.org" summary="Extensible Markup Language (XML)" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="game" type="String" %}
e.g. "minecraft" (optional)
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
<sites>
    <site>
        <domain>example.com</domain>
        <notes>Malware alert!</notes>
        <path>/</path>
        <reason>Illegal redistribution</reason>
    </site>
    ...
</sites>
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/{game}/sites.yaml" baseUrl="https://api.stopmodreposts.org" summary="YAML Ain't Markup Language (YAML)" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="game" type="String" %}
e.g. "minecraft" (optional)
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
- domain: example.com
  notes: Malware alert!
  path: /
  reason: Illegal redistribution
  ...
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/{game}/sites.txt" baseUrl="https://api.stopmodreposts.org" summary="Plain text" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="game" type="String" %}
e.g. "minecraft" (optional)
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
example.com
example.net
example.org
...
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/{game}/hosts.txt" baseUrl="https://api.stopmodreposts.org" summary="Hosts file (HOSTS.TXT)" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="game" type="String" %}
e.g. "minecraft" (optional)
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
# Informational header at the top of the file

0.0.0.0	example.com
0.0.0.0	example.net
0.0.0.0	example.org
...
0.0.0.0	www.example.com
0.0.0.0	www.example.net
0.0.0.0	www.example.org
...

# === End of StopModReposts site list ===
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/{game}/ublacklist.txt" baseUrl="https://api.stopmodreposts.org" summary="uBlacklist format" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="game" type="String" %}
e.g. "minecraft" (optional)
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
*://*.example.com/*
*://*.example.net/*
*://*.example.org/*
```
{% endswagger-response %}
{% endswagger %}
