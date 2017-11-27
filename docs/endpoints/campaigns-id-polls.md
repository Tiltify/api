# GET /campaigns/:id/polls

Retrieves the [polls](/entities/poll.md) and their associated options for a campaign.

```js
{
  "meta": {
    "status": 200
  },
  "data": [
    {
      "id": 47,
      "name": "Should pineapple go on pizza?",
      "active": true,
      "campaignId": 1337,
      "createdAt": 1498169329000,
      "updatedAt": 1498169329000,
      "options":[
        {
          "id": 42,
          "pollId": 47,
          "name":"No",
          "totalAmountRaised": 50,
          "createdAt": 1498169329000,
          "updatedAt": 1498169329000
        },
        {
          "id": 44,
          "pollId": 47,
          "name":"Yes",
          "totalAmountRaised": 50,
          "createdAt": 1498169329000,
          "updatedAt": 1498169329000
        }
      ]
    },
    {
      // ...
    }
  ]
}
```

## Examples

{% method %}
### GET /campaigns/42/polls
Returns a list of polls with the campaign ID of 42.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/campaigns/42/polls
```

{% endmethod %}
