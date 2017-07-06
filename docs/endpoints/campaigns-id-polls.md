# GET /campaigns/:id/polls

Retrieves the polls for a campaign.

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
      "options":[  
        {  
          "name":"No",
          "amount": 9001,
          "percentage": 100
        },
        {  
          "name":"Yes",
          "amount": 0,
          "percentage": 0
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

{% sample lang="js" %}
```js
try {
  const polls = await Tiltify.Campaign.get_polls(42)
  // do something with the polls
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  polls = Tiltify::Campaign.get_polls(42)
  # do something with the polls
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Campaign.get_polls(42) do
  {:ok, polls} -> # do something with the polls
  {:error, error} -> # handle error
end
```

{% endmethod %}
