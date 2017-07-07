# GET /challenges

Returns a list of challenges on Tiltify. This is a paginated endpoint.

```js
{
  "meta": {
    "status": 200
  },
  "data": [
    {
      "id": 466,
      "name": "Bounty hunters! We don't need this scum.",
      "amount": 91,
      "totalAmountRaised": 186,
      "active": true,
      "activatesOn": 1498169329000,
      "campaignId": 231,
      "endsAt": 1505762373000,
      "createdAt": 1498232189000
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
### GET /challenges
Returns a list of the first 100 challenges by default

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/challenges
```

{% sample lang="js" %}
```js
try {
  const challenges = await Tiltify.Challenge.index()
  // do something with the challenges
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  challenges = Tiltify::Challenge.index()
  # do something with the challenges
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Challenge.index() do
  {:ok, challenges} -> # do something with the challenges
  {:error, error} -> # handle error
end
```

{% endmethod %}
