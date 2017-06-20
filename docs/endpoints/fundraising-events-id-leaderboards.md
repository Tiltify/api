# GET /fundraising-events/:id/leaderboards

If the cause has allowed fundraising event leaderboards to be visible
this endpoint will return said leaderboards with up to 25 entries per.

```js

{
  "meta": {
    "status": 200
  },
  "data": {
    "individual": [
      {
        "userId": 2494,
        "name": "iKasperr",
        "url": "https://tiltify.com/@ikasperr",
        "amount_raised": 128930
      },
      // ...
    ],
    "team": [
      {
        "teamId": 387,
        "name": "DerpSquad",
        "url": "https://tiltify.com/+derpsquad",
        "amount_raised": 50493
      },
      // ...
    ],
  }
}
```

## Examples

{% method %}
### GET /fundraising-events/35/leaderboards
Returns a list of leaderboards with the fundraising event ID of 35.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/fundraising-events/35/leaderboards
```

{% sample lang="js" %}
```js
try {
  const leaderboards = await Tiltify.FundraisingEvents.leaderboards(35)
  // do something with the leaderboards
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  leaderboards = Tiltify::FundraisingEvents.leaderboards(35)
  # do something with the leaderboards
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.FundraisingEvents.leaderboards(35) do
  {:ok, leaderboards} -> # do something with the leaderboards
  {:error, error} -> # handle error
end
```

{% endmethod %}
