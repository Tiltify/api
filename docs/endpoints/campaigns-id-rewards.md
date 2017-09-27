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

{% sample lang="js" %}
```js
try {
  const rewards = await Tiltify.Campaign.get_rewards(42)
  // do something with the rewards
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  rewards = Tiltify::Campaign.get_rewards(42)
  # do something with the rewards
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Campaign.get_rewards(42) do
  {:ok, rewards} -> # do something with the rewards
  {:error, error} -> # handle error
end
```

{% endmethod %}
