# Validation Check API

{% api-method method="get" host="https://www.gadaga.io:10010" path="/api/v1/user/valid" %}
{% api-method-summary %}
Validation Check
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="value" type="string" required=true %}
validation value
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
Validation Type  
EMAIL, NICKNAME, PHONE
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



