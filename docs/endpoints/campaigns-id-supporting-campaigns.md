>### Deprecation Notice
>Api V3 is being deprecated on July 1st, 2023. Please consider updating to V5

>[V5 Api Documentation](https://v5api.tiltify.com/api/public)

-----

# GET /campaigns/:id/supporting-campaigns

Retrieves supporting campaigns given an identifier.
Resources that do not belong to a team will return an empty list/array.

```js
{
  "meta": {
    "status": 200
  },
  "data": [
    {
      "id": 1,
      "name": "My Awesome Campaign",
      "slug": "my-awesome-campaign",
      "url": "https://tiltify.com/@username/my-awesome-campaign",
      "description": "My awesome weekend campaign.",
      "thumbnail": {
        "src": "https://asdf.cloudfront.net/asdf.jpg",
        "alt": "synthesize distributed solutions",
        "width": 200,
        "height": 200
      },
      "causeId": 17,
      "userId": 14,
      "teamId": null,
      "fundraisingEventId": 39,
      "goal": 10000,
      "originalGoal": 5000,
      "amountRaised": 8923,
      "totalAmountRaised": 12325,
      "startsOn": "2017-03-24",
      "endsOn": "2017-03-26"
    },
    {
      "id": 2,
      "name": "My Awesome Campaign",
      "slug": "my-awesome-campaign",
      "url": "https://tiltify.com/@username/my-awesome-campaign",
      "description": "My awesome weekend campaign.",
      "thumbnail": {
        "src": "https://asdf.cloudfront.net/asdf.jpg",
        "alt": "synthesize distributed solutions",
        "width": 200,
        "height": 200
      },
      "causeId": 17,
      "userId": 14,
      "teamId": null,
      "fundraisingEventId": 39,
      "goal": 10000,
      "originalGoal": 5000,
      "amountRaised": 8923,
      "totalAmountRaised": 12325,
      "startsOn": "2017-03-24",
      "endsOn": "2017-03-26"
    }
  ]
}
```

## Examples

{% method %}
### GET /campaigns/42/supporting-campaigns
Returns supporting-campaigns campaign entity with the ID of 42.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/campaigns/42
```
{% endmethod %}
---

{% method %}
### GET /campaigns/campaign-slug/supporting-campaigns
Returns a single campaign entity with a slug of campaign-slug. Note that it
will pull the first campaign found with this slug. This is typically not the
expected result and you should instead pass a reference to a user

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/campaigns/campaign-slug/supporting-campaigns
```

{% endmethod %}
