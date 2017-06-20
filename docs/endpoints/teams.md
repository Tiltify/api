# GET /teams/:id

Retrieves a list of team entities.

```js
{
  "meta": {
    "status": 200
  },
  "data": [
    {
      "id": 387,
      "name": "DerpSquad",
      "slug": "derpsquad",
      "url": "https://tiltify.com/+derpsquad",
      "bio": "",
      "inviteOnly": true,
      "disbanded": false,
      "social": {
        "facebook": "tradechatonyoutube",
        "twitch": "tradechat",
        "twitter": "tradechat",
        "website": "",
        "youtube": "tradechat"
      },
      "avatar": {
        "src": "https://asdf.cloudfront.net/asdf.jpg",
        "alt": "",
        "width": 200,
        "height": 200
      }
    },
    // ...
  ]
}
```

## Examples

{% method %}
### GET /teams
Returns a list of teams.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/teams
```

{% sample lang="js" %}
```js
try {
  const teams = await Tiltify.Team.index()
  // do something with the teams
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  teams = Tiltify::Team.index()
  # do something with the teams
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Team.index() do
  {:ok, teams} -> # do something with the teams
  {:error, error} -> # handle error
end
```

{% endmethod %}
