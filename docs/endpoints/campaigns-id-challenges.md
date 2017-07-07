# GET /campaigns/:id/challenges

Retrieves the challenges for a campaign.

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
}
```

## Examples

{% method %}
### GET /campaigns/42/challenges
Returns a list of challenges with the campaign ID of 42.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/campaigns/42/challenges
```

{% sample lang="js" %}
```js
try {
  const challenges = await Tiltify.Campaign.get_challenges(42)
  // do something with the challenges
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  challenges = Tiltify::Campaign.get_challenges(42)
  # do something with the challenges
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Campaign.get_challenges(42) do
  {:ok, challenges} -> # do something with the challenges
  {:error, error} -> # handle error
end
```

{% endmethod %}
