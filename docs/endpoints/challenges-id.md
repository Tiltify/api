# GET /challenges/:id

Retrieves a single challenge given an identifier.

```js
{
  "meta": {
    "status": 200
  },
  "data": {
    "id": 466,
    "name": "Bounty hunters! We don't need this scum.",
    "amount": 91,
    "totalAmountRaised": 186,
    "active": true,
    "activatesOn": 1498169329000,
    "campaignId": 231,
    "endsAt": 1505762373000,
    "createdAt": 1498232189000
  }
}
```

## Examples

{% method %}
### GET /challenges/387
Returns a single challenge entity with the ID of 387.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/challenges/387
```

{% sample lang="js" %}
```js
try {
  const challenge = await Tiltify.Challenge.get(387)
  // do something with the challenge
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  challenge = Tiltify::Challenge.get(387)
  # do something with the challenge
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Challenge.get(387) do
  {:ok, challenge} -> # do something with the challenge
  {:error, error} -> # handle error
end
```

{% endmethod %}
