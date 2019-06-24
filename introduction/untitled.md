# Authentication

The Schools API uses API Keys to authenticate requests.  You can view and manage your API key in the [SchoolsAPI Dashboard](https://schoolsapi.com/home).

Your API keys should be treated like passwords.  They are private and should be kept secure!  Do not share your secret API keys in publicly accessible areas such as Github, client-side code, and so on.

### Header Authorization

To use your API key you must supply it as a `X-Auth-Token` parameter in your request header.

**Example:**

```text
https://schoolsapi.com/api/v1/us/name?token=4eVmcmeXkiMQJ&state=oh&name=Example School
```

All API requests must be made over HTTPS.  We do not accept calls made over plain HTTP.  Those calls will be rejected, and your API requests will fail.

