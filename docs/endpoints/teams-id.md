# GET /teams/:id

Retreives a single team given an identifier.

```js
{
  "meta": {
    "status": 200
  },
  "data": {
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
  }
}
```

## Examples

{% method %}
### GET /teams/387
Returns a single team entity with the ID of 387.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/teams/387
```

{% sample lang="js" %}
```js
try {
  const team = await Tiltify.Team.get(387)
  // do something with the team
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  team = Tiltify::Team.get(387)
  # do something with the team
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Team.get(42) do
  {:ok, team} -> # do something with the team
  {:error, error} -> # handle error
end
```

{% endmethod %}

---

{% method %}
### GET /teams/derpsquad
Returns a single team entity with a slug of derpsquad.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/teams/derpsquad
```

{% sample lang="js" %}
```js
try {
  const team = await Tiltify.Team.get('derpsquad')
  // do something with the team
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  team = Tiltify::Team.get('derpsquad')
  # do something with the team
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Team.get("derpsquad") do
  {:ok, team} -> # do something with the team
  {:error, error} -> # handle error
end
```

{% endmethod %}

