# Postal Code

{% hint style="info" %}
The base URL for all requests is https://schoolsapi.com/api/v1
{% endhint %}

{% api-method method="get" host="https://schoolsapi.com" path="/api/v1/name/country\_code" %}
{% api-method-summary %}
Name
{% endapi-method-summary %}

{% api-method-description %}
This method allows you to lookup a school by name.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="country\_code" type="string" required=true %}
 The country you are looking for the school in. \(ex. us, ca, etc.\)
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="X-Auth-Token" type="string" required=true %}
Your authorization API key from your dashboard.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="name" type="string" required=true %}
The name of the school you are requesting.
{% endapi-method-parameter %}

{% api-method-parameter name="state" type="string" required=false %}
The state of the school. This can help narrow your search.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
This example response was from requesting "Palo Alto High" in the name endpoint.
{% endapi-method-response-example-description %}

{% code-tabs %}
{% code-tabs-item title="Name\_Response" %}
```
{
    "data": [
        {
            "id": 12489,
            "name": "Palo Alto High",
            "level": "High",
            "state_name": "California",
            "country_code": "US",
            "addresses": {
                "mailing": {
                    "street1": "50 Embarcadero Rd.",
                    "street2": "",
                    "street3": "",
                    "city": "Palo Alto",
                    "state": "CA",
                    "postal": "94301",
                    "postal_4": "2321"
                },
                "physical": {
                    "street1": "50 Embarcadero Rd.",
                    "street2": "",
                    "street3": "",
                    "city": "Palo Alto",
                    "state": "CA",
                    "postal": "94301",
                    "postal_4": "2321"
                }
            },
            "phone_number": "(650)329-3701",
            "website": "",
            "school_type": "Regular School",
            "school_type_id": "1"
        }
    ]
}
```
{% endcode-tabs-item %}
{% endcode-tabs %}
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}
