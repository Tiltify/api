# GET /causes/:id/donations

Authenticated and paginated endpoint to retrieve the donations for a cause.

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
### GET /causes/35/donations
Returns the donations for the cause with an ID of 35.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/causes/35/donations
```

{% endmethod %}
