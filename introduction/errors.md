# Errors

SchoolsAPI uses conventional HTTP response codes to indicate success or failure of an API request.

The following can be assumed:

* `2xx` range indicates a success.
* `4xx` range indicates an error that failed given the information provided \(ex. a parameter is missing, no header token supplied, etc\).
* `5xx` range indicates an error on SchoolAPI's servers \(these are rare\).

All errors will return a message stating what error occurred.  You'll want to validate the response code for easier handling.

#### Example:

```text
{
    "status": "failure",
    "data": {
        "message": "An API key could not be found in the header of your request."
    }
}
```

