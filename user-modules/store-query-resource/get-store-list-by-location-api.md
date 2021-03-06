# Get Store List By Location API

{% api-method method="get" host="https://www.gadaga.io:10010" path="/api/v1/stores" %}
{% api-method-summary %}
Get Stores By Location
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="coordinates" type="object" required=true %}
include latitude: Double, longitude: Double
{% endapi-method-parameter %}

{% api-method-parameter name="distance" type="number" required=true %}
double  
distance is kilometer
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```kotlin
data class ResponseStore (
        val id: String,
        val name: String,
        val thumbnailUrl: String,
        val rate: Double,
        val category: String,
        val coordinates: LatLon,
        val menuCategories: List<ResponseStoreMenuCategory>,
        val menus: Map<String, List<ResponseStoreMenu>>,
        val origin: String,
        val reviews: List<ResponseStoreReview>?,
        val info: ResponseStoreInfo
)

data class ResponseStoreMenuCategory(
        val id: String,
        val name: String,
        val order: Int
)

data class ResponseStoreMenu(
        val id: String,
        val name: String,
        val description: String?,
        val imageUrl: String?,
        val price: Int,
        val cookingTime: Int,
        val order: Int,
        val optionCategories: List<ResponseStoreMenuOptionCategory>,
        val options: Map<String, List<ResponseStoreMenuOption>>
)

data class ResponseStoreMenuOptionCategory(
        val id: String,
        val name: String,
        val isRequired: Boolean,
        val selectableCount: Int,
        val order: Int
)

data class ResponseStoreMenuOption(
        val id: String,
        val name: String,
        val price: Int,
        val order: Int
)

data class ResponseStoreReview(
        val id: String,
        val userName: String,
        val rate: Int,
        val createdAt: String,
        val content: String,
        val imageUrls: List<String>?,
        val repliedReviewId: String
)
data class ResponseStoreInfo(
        val photoUrls: List<String>?,
        val address: String,
        val operationHour: List<ResponseStoreTime>,
        val breakTime: List<ResponseStoreTime>?,
        val storeNumber: String,
        val holiday: String,
        val businessInfo: ResponseBusinessInfo
)

data class ResponseBusinessInfo (
        val businessName: String,
        val businessOwner: String,
        val businessAddress: String,
        val businessNumber: String
)

data class ResponseStoreTime(
        val day: String,
        val start: Int,
        val end: Int
)

data class LatLon (
        val latitude: Double,
        val longitude: Double
)

return List<ResponseStore>
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



