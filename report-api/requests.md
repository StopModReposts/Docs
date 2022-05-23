# Requests

{% swagger method="get" path="/api/v1/waitlist" baseUrl="https://report.stopmodreposts.org" summary="Get Waitlist" %}
{% swagger-description %}
The waitlist is a list of sites which are waiting for review. These sites cannot be submitted until they're of the waitlist (reviewed).
{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}
```javascript
[
  {
    "domain": "example.com",
    "type": "report",
    "timestamp": "2022-05-23 17:27:30.324524"
  },
  ...
]

```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/api/v1/blacklist" baseUrl="https://report.stopmodreposts.org" summary="Get Blacklist" %}
{% swagger-description %}
The blacklist is a list of (manually) blocked domains. These domains cannot be submitted.
{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}
```javascript
[
  {
    "domain": "example.com"
  },
  ...
]
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="/api/v1/report" baseUrl="https://report.stopmodreposts.org" summary="Post Report" %}
{% swagger-description %}
Post a site report or a false-positive report to this endpoint to get it reviewed by us.
{% endswagger-description %}

{% swagger-response status="201: Created" description="Success" %}
```javascript
{
    "detail": "Success!",
    "already_listed": False,
    "under_review": False,
    "blacklist": False,
    "data": {
        "domain": "example.com",
        "description": "Test description",
        "false-positive": False | True
    }
}
```
{% endswagger-response %}

{% swagger-response status="409: Conflict" description="Domain already listed or on waitinglist" %}
```javascript
{
    "detail": "Failed to report - domain already listed",
    "already_listed": False | True,
    "under_review": False | True,
    "blacklist": False,
    "data": {
        "domain": "example.com",
        "description": "Test description",
        "false-positive": False | True
    }
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Domain on blacklist" %}
```javascript
{
    "detail": "Failed to report - domain blacklisted",
    "already_listed": False,
    "under_review": False,
    "blacklist": True,
    "data": {
        "domain": "example.com",
        "description": "Test description",
        "false-positive": False | True
    }
}
```
{% endswagger-response %}
{% endswagger %}
