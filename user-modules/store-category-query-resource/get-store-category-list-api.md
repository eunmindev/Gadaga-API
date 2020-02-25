# Get Store Category List API

{% api-method method="get" host="https://www.gadaga.io:10010" path="/api/v1/store-categories" %}
{% api-method-summary %}
Get Store Categories
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```kotlin
data class ResponseStoreCategory (
        val id: Long,
        val categoryName: String,
        val categoryIdentity: String,
        val orderBy: Int
)

return List<ResponseStorecategory>
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



