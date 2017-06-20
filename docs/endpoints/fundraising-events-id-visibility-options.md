# /fundraising-events/:id/visibility-options

Retrieves and updates the visibility options for a cause. These options are
used to determine the visibility of certain features on the frontend of the
website. These options also disable features in the API such as whether or not
a user can donate directly to a cause, or whether the leaderboards are
publically available.

```js
{
  "meta": {
    "status": 200
  },
  "data": {
    "startsAt": {
      "visible": true
    },
    "endsAt": {
      "visible": true
    },
    "fundraiserGoalAmount": {
      "visible": true,
      "type": "BOTH"
    },
    "individualLeaderboard": {
      "visible": true
    },
    "teamLeaderboard": {
      "visible": true,
      "type": "ALL"
    },
    "donorLeaderboard": {
      "visible": true,
      "type": "ALL"
    },
    "preventDonationsBeforeStart": {
      "visible": false
    },
    "registration": {
      "visible": false
    },
    "donate": {
      "visible": true
    }
  }
}
```

## Examples

{% method %}
### GET /fundraising-events/35/visibility-options
Returns visibility options for a fundraising event with the ID of 35

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/fundraising-events/35/visibility-options
```

{% sample lang="js" %}
```js
try {
  const visibilityOptions = await Tiltify.FundraisingEvent.visibilityOptions(35)
  // do something with the visibilityOptions
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  visibility_options = Tiltify::FundraisingEvent.visibility_options(35)
  # do something with the visibility options
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.FundraisingEvent.visibility_options(35) do
  {:ok, visibility_options} -> # do something with the visibility_options
  {:error, error} -> # handle error
end
```

{% endmethod %}

---

{% method %}
### PATCH /fundraising-events/35/visibility-options
Update the visibility of the donate button on the fundraising event page for
the fundraising event with id of 35.

{% sample lang="curl" %}
```bash
curl -X PATCH \
  -H 'Content-Type: application/json' \
  -d '{"donate": { "visible": false }}' \
  https://tiltify.com/api/v3/fundraising-events/35/visibility-options
```

{% sample lang="js" %}
```js
try {
  const visibilityOptions = await Tiltify.FundraisingEvent.VisibilityOptions.patch(35, { donate: { visible: false } })
  // do something with the visibilityOptions
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  visibility_options = Tiltify::FundraisingEvent::VisibilityOptions.patch(35, donate: { visible: false })
  # do something with the visibility options
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.FundraisingEvent.VisibilityOptions.patch(35, donate: { visible: false } ) do
  {:ok, visibility_options} -> # do something with the visibility_options
  {:error, error} -> # handle error
end
```

{% endmethod %}
