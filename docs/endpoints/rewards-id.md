# GET /rewards/:id

Retrieves a single reward given an identifier.

```js
{
  "meta": {
    "status": 200
  },
  "data": {
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
  }
}
```

## Examples

{% method %}
### GET /rewards/387
Returns a single reward entity with the ID of 387.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/rewards/387
```

{% sample lang="js" %}
```js
try {
  const reward = await Tiltify.Reward.get(387)
  // do something with the reward
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  reward = Tiltify::Reward.get(387)
  # do something with the reward
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Reward.get(42) do
  {:ok, reward} -> # do something with the reward
  {:error, error} -> # handle error
end
```

{% endmethod %}
