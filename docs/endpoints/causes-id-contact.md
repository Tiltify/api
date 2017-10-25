# /causes/:id/contact

Retrieves the publically available contact information for a cause.

```js
{
  "meta": {
    "status": 200
  },
  "data": {
    "legalName": "Good Cause Inc.",
    "email": "dev@tiltify.com",
    "twitter": "tiltify",
    "youtube": "tiltify",
    "facebook": "tiltify",
    "instagram": "tiltify",
    "snapchat": "tiltify",
    "address": {
      "addressLine1": "123 Some St",
      "addressLine2": "",
      "city": "Houston",
      "region": "TX",
      "postalCode": "77008",
      "country": "US"
    }
  }
}
```

## Examples

{% method %}
### GET /causes/35/contact
Returns the contact information for a given cause

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/causes/35/contact
```

{% endmethod %}
