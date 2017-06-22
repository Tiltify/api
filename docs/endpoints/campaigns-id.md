# GET /campaigns/:id

Retrieves a single campaign given an identifier.

```js
{
  "meta": {
    "status": 200
  },
  "data": {
    "id": 1,
    "name": "My Awesome Campaign",
    "slug": "my-awesome-campaign",
    "url": "https://tiltify.com/@username/my-awesome-campaign",
    "description": "My awesome weekend campaign.",
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
    "goal": 10000,
    "originalGoal": 5000,
    "amountRaised": 8923,
    "totalAmountRaised": 12325,
    "startsOn": "2017-03-24",
    "endsOn": "2017-03-26"
  }
}
```

## Examples

{% method %}
### GET /campaigns/42
Returns a single campaign entity with the ID of 42.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/campaigns/42
```

{% sample lang="js" %}
```js
try {
  const campaign = await Tiltify.Campaign.get(42)
  // do something with the campaign
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  campaign = Tiltify::Campaign.get(42)
  # do something with the campaign
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Campaign.get(42) do
  {:ok, campaign} -> # do something with the campaign
  {:error, error} -> # handle error
end
```

{% endmethod %}

---

{% method %}
### GET /campaigns/campaign-slug
Returns a single campaign entity with a slug of campaign-slug. Note that it
will pull the first campaign found with this slug. This is typically not the
expected result and you should instead pass a reference to a user

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/campaigns/campaign-slug
```

{% sample lang="js" %}
```js
try {
  const campaign = await Tiltify.Campaign.get('campaign-slug')
  // do something with the campaign
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  campaign = Tiltify::Campaign.get('campaign-slug')
  # do something with the campaign
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Campaign.get("campaign-slug") do
  {:ok, campaign} -> # do something with the campaign
  {:error, error} -> # handle error
end
```

{% endmethod %}

---

{% method %}
### GET /campaigns/campaign-slug
Returns a single campaign entity with a slug of campaign-slug. Note that it
will pull the first campaign found with this slug. This is typically not the
expected result and you should instead pass a reference to a user

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/campaigns/campaign-slug
```

{% sample lang="js" %}
```js
try {
  const campaign = await Tiltify.Campaign.get('campaign-slug')
  // do something with the campaign
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  campaign = Tiltify::Campaign.get('campaign-slug')
  # do something with the campaign
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Campaign.get("campaign-slug") do
  {:ok, campaign} -> # do something with the campaign
  {:error, error} -> # handle error
end
```

{% endmethod %}

---

{% method %}
### GET /campaigns/campaign-slug?username=ben
Returns a single campaign entity with a slug of campaign-slug belonging to the
user with a username of ben.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/campaigns/campaign-slug?username=ben
```

{% sample lang="js" %}
```js
try {
  const campaign = await Tiltify.Campaign.get({ slug: 'campaign-slug', username: 'ben' })
  // do something with the campaign
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  campaign = Tiltify::Campaign.get(slug: 'campaign-slug', username: 'ben')
  # do something with the campaign
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Campaign.get(slug: "campaign-slug", username: "ben") do
  {:ok, campaign} -> # do something with the campaign
  {:error, error} -> # handle error
end
```

{% endmethod %}

---

{% method %}
### GET /campaigns/campaign-slug?userId=37
Returns a single campaign entity with a slug of campaign-slug belonging to the
user with an id of 37

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/campaigns/campaign-slug?userId=37
```

{% sample lang="js" %}
```js
try {
  const campaign = await Tiltify.Campaign.get({ slug: 'campaign-slug', userId: 37 })
  // do something with the campaign
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  campaign = Tiltify::Campaign.get(slug: 'campaign-slug', user_id: 37)
  # do something with the campaign
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Campaign.get(slug: "campaign-slug", user_id: 37) do
  {:ok, campaign} -> # do something with the campaign
  {:error, error} -> # handle error
end
```

{% endmethod %}
