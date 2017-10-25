# GET /fundraising-events/:id/schedule

Endpoint to retrieve the schedule for a fundraising event.

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
### GET /fundraising-events/35/schedule
Returns the schedule for the fundraising event with an ID of 35.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/fundraising-events/35/schedule
```

{% endmethod %}
