# GET /teams/:id/campaigns

Retrieves the campaigns which are part of a team.

```js
{
  "meta": {
    "status": 200
  },
  "data": [
    {
      "name": "My Awesome Campaign",
      "slug": "my-awesome-campaign",
      "url": "https://tiltify.com/@username/my-awesome-campaign",
      "description": "My awesome weekend campaign.\n Save the kids.",
      "thumbnail": "https://asdfasdfasdf.cloudfront.net/1234.jpg",
      "causeId": 17,
      "userId": 14,
      "teamId": 35,
      "fundraisingEventId": 39,
      "currency": "USD",
      "goal": 10000,
      "originalGoal": 5000,
      "amountRaised": 8923,
      "totalAmountRaised": 12325,
      "startsOn": "2017-03-24",
      "endsOn": "2017-03-26"
    },
    // ...
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
### GET /teams/35/campaigns
Returns the campaigns for the team with an ID of 35.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/teams/35/campaigns
```

{% sample lang="js" %}
```js
try {
  const campaigns = await Tiltify.Team.campaigns(35)
  // do something with the campaigns
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  campaigns = Tiltify::Team.campaigns(35)
  # do something with the campaigns
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Team.campaigns(35) do
  {:ok, campaigns} -> # do something with the campaigns
  {:error, error} -> # handle error
end
```

{% endmethod %}
