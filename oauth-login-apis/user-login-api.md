---
description: 'Gadaga, Social Users Login'
---

# User Login API

{% api-method method="get" host="https://www.gadaga.io:10000" path="/api/v1/oauth/user" %}
{% api-method-summary %}
User Login API
{% endapi-method-summary %}

{% api-method-description %}
user login api
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="password" type="string" required=false %}
use : gadaga
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=false %}
use : gadaga
{% endapi-method-parameter %}

{% api-method-parameter name="uid" type="string" required=false %}
social id  
use : social
{% endapi-method-parameter %}

{% api-method-parameter name="socialType" type="string" required=true %}
GADAGA, NAVER, KAKAO, GOOGLE  
use : gadaga, social
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Login successfully
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
    "accessToken" : "access token example",
    "refreshToken" : "refresh token example"
}
```
{% endtab %}
{% endtabs %}
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    "message": "Ain't no cake like that."}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



