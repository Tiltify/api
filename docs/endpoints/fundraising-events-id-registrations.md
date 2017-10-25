# GET /fundraising-events/:id/registrations

This is an authorization required endpoint which returns the registrations made
to a specific fundraising event.

```js
{
  "meta": {
    "status": 200
  },
  "data": [
    {
      "id": 4,
      "userId": 9444,
      "email": "dev@tiltify.com",
      "subscribed": true,
      "registeredAt": "2017-04-07T12:10:16.364-04:00",
      "address": {
        "addressLine1": "123 Over there",
        "addressLine2": "#123",
        "city": "Houston",
        "state": "TX",
        "postalCode": "12345",
      },
      "shirtSize": "M",
      "serviceHours": false
    },
    // ...
  ]
}
```

## Examples

{% method %}
### GET /fundraising-events/1/registrations
Returns the registration field settings for a fundraising event with an id of 1.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/fundraising-events/1/registrations
```

{% endmethod %}
