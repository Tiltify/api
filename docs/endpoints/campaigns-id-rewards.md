# GET /campaigns/:id/rewards

Retrieves the rewards for a campaign.

```js
{
  "meta": {
    "status": 200
  },
  "data": [
    {
      "id": 1,
      "alwaysActive": true,
      "name": "Fingerstache vhs paleo tattooed echo cold-pressed.",
      "amount": 43,
      "kind": "virtual",
      "quantity": null,
      "remaining": null,
      "fairMarketValue": 88,
      "startsAt": null,
      "endsAt": 1511264923000,
      "description": "Chuck Norris can access the DB from the UI.",
      "shippingAddressRequired": false,
      "shippingNote": null,
      "image": {
        "src": "",
        "alt": "Chuck Norris can access the DB from the UI.",
        "width": 200,
        "height": 200
      },
      "currency": "USD",
      "createdAt": 1498169329000
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
