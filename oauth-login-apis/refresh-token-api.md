# Refresh Token API

{% api-method method="post" host="https://www.gadaga.io:10000" path="/api/v1/oauth/refresh" %}
{% api-method-summary %}
Get Refresh Token
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-form-data-parameters %}
{% api-method-parameter name="refreshToken" type="string" required=true %}
refresh token obtained when logging in
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

{% tabs %}
{% tab title="Kotlin" %}
```kotlin
data class ResponseToken (
        val accessToken: String,
        val refreshToken: String
)
```
{% endtab %}

{% tab title="Json" %}
```
{
    "accessToken" : "String",
    "refreshToken" : "String"
}
```
{% endtab %}
{% endtabs %}
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



