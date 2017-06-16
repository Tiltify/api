# GET /campaigns/:id/donations

Retrieves the most recent donations for a campaign in descending order

```js
{
  meta: {
    status: 200
  },
  data: [
    {
      // Donation
    },
    {
      // Donation
    },
  ],
  links: {
    next: "",
    prev: "",
    self: "",
    first: "",
    last: "",
  }

}
```

## Examples

{% method %}
### GET /campaigns/42/donations
Returns a list of donations entities with the campaign ID of 42 in decending order.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/campaigns/42/donations
```

{% sample lang="js" %}
```js
try {
  const campaign = await Tiltify.Campaign.get_donations(42)
  // do something with the campaign
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  campaign = Tiltify::Campaign.get_donations(42)
  # do something with the campaign
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Campaign.get_donations(42) do
  {:ok, campaign} -> # do something with the campaign
  {:error, error} -> # handle error
end
```

{% endmethod %}

