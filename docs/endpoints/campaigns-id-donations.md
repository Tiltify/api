>### Deprecation Notice
>Api V3 is being deprecated on July 1st, 2023. Please consider updating to V5

>[V5 Api Documentation](https://v5api.tiltify.com/api/public)

-----

# GET /campaigns/:id/donations

Retrieves the most recent donations for a campaign in descending order. An
object with the minimum required information is shown. There may be a pointer
to an incentive if it exists.

```js
{
  "meta": {
    "status": 200
  },
  "data": [
    {
      "id": 21347,
      "amount": 4.20,
      "name": "Yoda",
      "comment": "Judge me by my size, do you?",
      "completedAt": 1490328000000,
      "rewardId": 12
    },
    {
      "id": 21342,
      "amount": 1.00,
      "name": "Me",
      "comment": "This is an easy Game",
      "completedAt": 1490327800000
    },
    // ...
  ],
  "links": {
    "prev": "",
    "next": "",
    "self": ""
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
