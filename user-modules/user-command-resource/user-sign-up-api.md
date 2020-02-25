# User Sign Up API

{% api-method method="post" host="https://www.gadaga.io:10010" path="/api/v1/user" %}
{% api-method-summary %}
Sign Up for User
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="nickname" type="string" required=true %}
user nickname
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=true %}
user 2mail
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" required=false %}
user passowrd  
use : gadaga
{% endapi-method-parameter %}

{% api-method-parameter name="socialId" type="string" required=false %}
user social id  
use : social
{% endapi-method-parameter %}

{% api-method-parameter name="socialType" type="string" required=true %}
user social type  
GADAGA, NAVER, KAKAO, GOOGLE
{% endapi-method-parameter %}

{% api-method-parameter name="phoneNumber" type="string" required=true %}
user phone number
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```kotlin
data class ResponseToken (
        val accessToken: String,
        val refreshToken: String
)
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



