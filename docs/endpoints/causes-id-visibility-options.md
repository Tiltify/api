# /causes/:id/visibility-options

Retrieves and updates the visibility options for a cause. These options are
used to determine the visibility of certain features on the frontend of the
website. These options also disable features in the API such as whether or not
a user can donate directly to a cause, or whether the leaderboards are
publically available.

```json
{
  "donate": {
    "visible": true
  },
  "individual_leaderboard": {
    "visible": true,
    "type": "ALL"
  },
  "team_leaderboard": {
    "visible": true,
    "type": "ALL"
  }
}
```

## Examples

{% method %}
### GET /causes/35/visibility-options
Returns a single campaign entity with the ID of 42.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/causes/35/visibility-options
```

{% sample lang="js" %}
```js
try {
  const visibilityOptions = await Tiltify.Cause.visibilityOptions(35)
  // do something with the visibilityOptions
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  visibility_options = Tiltify::Cause.visibility_options(35)
  # do something with the visibility options
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Cause.visibility_options(35) do
  {:ok, visibility_options} -> # do something with the visibility_options
  {:error, error} -> # handle error
end
```

{% endmethod %}

---

{% method %}
### PATCH /causes/35/visibility-options
Update the visibility of the donate button on the cause page for the cause with
id of 35.

{% sample lang="curl" %}
```bash
curl -X PATCH \
  -H 'Content-Type: application.json' \
  -d '{"donate": { "visible": false }}' \
  https://tiltify.com/api/v3/causes/35/visibility-options
```

{% sample lang="js" %}
```js
try {
  const visibilityOptions = await Tiltify.Cause.VisibilityOptions.patch(35, { donate: { visible: false } })
  // do something with the visibilityOptions
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  visibility_options = Tiltify::Cause::VisibilityOptions.patch(35, donate: { visible: false })
  # do something with the visibility options
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Cause.VisibilityOptions.patch(35, donate: { visible: false } ) do
  {:ok, visibility_options} -> # do something with the visibility_options
  {:error, error} -> # handle error
end
```

{% endmethod %}
