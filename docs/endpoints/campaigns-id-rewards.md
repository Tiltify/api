>### Deprecation Notice
>Api V3 is being deprecated on July 1st, 2023. Please consider updating to V5

>[V5 Api Documentation](https://v5api.tiltify.com/api/public)

-----

# GET /campaigns/:id/rewards

Retrieves all [rewards](/entities/reward.md) for a campaign.

```js
{
  "meta": {
    "status": 200
  },
  "data": [
    {
      "id": 1,
      "name": "Fingerstache vhs paleo tattooed echo cold-pressed.",
      "description": "Chuck Norris can access the DB from the UI.",
      "amount": 43,
      "kind": "virtual",
      "quantity": null,
      "remaining": null,
      "fairMarketValue": 88,
      "currency": "USD",
      "shippingAddressRequired": false,
      "shippingNote": null,
      "image": {
        "src": "",
        "alt": "Chuck Norris can access the DB from the UI.",
        "width": 270,
        "height": 176
      },
      "active": true,
      "startsAt": 0,
      "createdAt": 1498169329000,
      "updatedAt": 1498249889000
    },
    {
      // ...
    }
  ]
}
```

## Examples

{% method %}
### GET /campaigns/42/rewards
Returns a list of rewards with the campaign ID of 42.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/campaigns/42/rewards
```

{% endmethod %}
