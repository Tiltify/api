# GET /causes/:id/campaigns

Retrieves the campaigns which support a cause.

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
      "thumbnail": {
        "src": "https://asdf.cloudfront.net/asdf.jpg",
        "alt": "synthesize distributed solutions",
        "width": 200,
        "height": 200
      },
      "causeId": 17,
      "userId": 14,
      "teamId": null,
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
### GET /causes/35/campaigns
Returns the campaigns for the cause with an ID of 35.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/causes/35/campaigns
```

{% sample lang="js" %}
```js
try {
  const campaigns = await Tiltify.Cause.campaigns(35)
  // do something with the campaigns
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  campaigns = Tiltify::Cause.campaigns(35)
  # do something with the campaigns
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Cause.campaigns(35) do
  {:ok, campaigns} -> # do something with the campaigns
  {:error, error} -> # handle error
end
```

{% endmethod %}
