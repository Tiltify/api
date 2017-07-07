# GET /campaigns/:id/schedule

Endpoint to retrieve the schedule for a campaign.

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

{% sample lang="js" %}
```js
try {
  const schedule = await Tiltify.Campaign.schedule(35)
  // do something with the schedule
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  schedule = Tiltify::Campaign.schedule(35)
  # do something with the schedule
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Campaign.schedule(35) do
  {:ok, schedule} -> # do something with the schedule
  {:error, error} -> # handle error
end
```

{% endmethod %}
