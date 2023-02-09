>### Deprecation Notice
>Api V3 is being deprecated on July 1st, 2023. Please consider updating to V5

>[V5 Api Documentation](https://v5api.tiltify.com/api/public)

-----

# GET /campaigns/:id/schedule

Endpoint to retrieve the [schedule](/entities/schedule.md) for a campaign.

```js
{
  "meta": {
    "status": 200
  },
  "data": [
    {
      "id": 1658,
      "name": "Second Day Starts",
      "description": "The Second Day of our event!",
      "startsAt": 1498107600000
    },
    // ...
  ]
}
```

## Examples

{% method %}
### GET /campaigns/35/schedule
Returns the schedule for the campaign with an ID of 35.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/campaigns/35/schedule
```

{% endmethod %}
