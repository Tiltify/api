# GET /rewards

Returns a list of rewards on Tiltify. This is a paginated endpoint.

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
  ],
  "links": {
    "prev": "",
    "next": "",
    "self": "",
    "first": "",
    "last": "",
  }
}
```

## Examples

{% method %}
### GET /rewards
Returns a list of the first 100 rewards by default

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/rewards
```

{% sample lang="js" %}
```js
try {
  const rewards = await Tiltify.Reward.index()
  // do something with the rewards
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  rewards = Tiltify::Reward.index()
  # do something with the rewards
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Reward.index() do
  {:ok, rewards} -> # do something with the rewards
  {:error, error} -> # handle error
end
```

{% endmethod %}
