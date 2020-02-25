# Find Email API

{% api-method method="get" host="https://www.gadaga.io:10010" path="/api/v1/user/find-email" %}
{% api-method-summary %}
Find Email
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="phoneNumber" type="string" required=true %}
phone number to find Email
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```kotlin
data class ResponseUser (
        val nickname: String = "",
        val email: String,
        val socialType: String,
        val phoneNumber: String = "",
        val createAt: String
)
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



