# Postal Code

{% hint style="info" %}
The base URL for all requests is [https://schoolsapi.com/api/v1](https://schoolsapi.com/api/v1)
{% endhint %}

{% api-method method="get" host="https://schoolsapi.com" path="/api/v1/:country\_code/postalcode/" %}
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
{% api-method-parameter name="postal\_code" type="string" required=true %}
The postal code of the school you are requesting.  
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
This example response was from requesting "90210" in the postalcode endpoint.
{% endapi-method-response-example-description %}

{% code-tabs %}
{% code-tabs-item title="Name\_Response" %}
```text
{
    "data": [
        {
            "id": 6962,
            "name": "El Rodeo Elementary",
            "level": "Elementary",
            "state": "CA",
            "country_code": "US",
            "addresses": {
                "mailing": {
                    "street1": "605 N. Whittier Dr.",
                    "street2": "",
                    "street3": "",
                    "city": "Beverly Hills",
                    "state": "CA",
                    "postal": "90210",
                    "postal_4": "3112"
                },
                "physical": {
                    "street1": "605 N. Whittier Dr.",
                    "street2": "",
                    "street3": "",
                    "city": "Beverly Hills",
                    "state": "CA",
                    "postal": "90210",
                    "postal_4": "3112"
                }
            },
            "phone_number": "(310)229-3670",
            "website": "",
            "school_type": "Regular School",
            "school_type_id": "1"
        },
        {
            "id": 6963,
            "name": "Hawthorne Elementary",
            "level": "Elementary",
            "state": "CA",
            "country_code": "US",
            "addresses": {
                "mailing": {
                    "street1": "624 N. Rexford Dr.",
                    "street2": "",
                    "street3": "",
                    "city": "Beverly Hills",
                    "state": "CA",
                    "postal": "90210",
                    "postal_4": "3312"
                },
                "physical": {
                    "street1": "624 N. Rexford Dr.",
                    "street2": "",
                    "street3": "",
                    "city": "Beverly Hills",
                    "state": "CA",
                    "postal": "90210",
                    "postal_4": "3312"
                }
            },
            "phone_number": "(310)229-3675",
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

