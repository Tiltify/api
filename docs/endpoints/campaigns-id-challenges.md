>### Deprecation Notice
>Api V3 is being deprecated on July 1st, 2023. Please consider updating to V5

>[V5 Api Documentation](https://v5api.tiltify.com/api/public)

-----

# GET /campaigns/:id/challenges

Retrieves the [challenges](/entities/challenge.md) for a campaign.

```js
{
  "meta": {
    "status": 200
  },
  "data": [
    {
      "id": 466,
      "name": "Bounty hunters! We don't need this scum.",
      "amount": 91,
      "totalAmountRaised": 186,
      "active": true,
      "activatesOn": 1498169329000,
      "campaignId": 231,
      "endsAt": 1505762373000,
      "createdAt": 1498232189000,
      "updatedAt": 1498232189000
    },
    {
      // ...
    }
  ],
}
```

## Examples

{% method %}
### GET /campaigns/42/challenges
Returns a list of challenges with the campaign ID of 42.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/campaigns/42/challenges
```

{% endmethod %}
