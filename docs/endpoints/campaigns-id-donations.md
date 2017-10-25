# GET /campaigns/:id/donations

Retrieves the most recent donations for a campaign in descending order

```js
{
  "meta": {
    "status": 200
  },
  "data": [
    {
      "id": 21347,
      "amount": 556.0,
      "name": "Yoda",
      "donorComment": "Judge me by my size, do you?",
      "createdAt": 1490328000000
    },
    // ...
  ],
  "links": {
    "prev": "",
    "next": "",
    "self": "",
    "first": "",
    "last": "",
  }
}
```

## Examples

{% method %}
### GET /campaigns/42/donations
Returns a list of donation entities with the campaign ID of 42 in decending order.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/campaigns/42/donations
```

{% endmethod %}
