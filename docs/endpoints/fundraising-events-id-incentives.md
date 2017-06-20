# GET /fundraising-events/:id/incentives

Endpoint to retrieve the incentives for a fundraising event.

```js
{
  "meta": {
    "status": 200
  },
  "data": [
    {
      "id": 1,
      "title": "A Special Incentive for the streamers",
      "description": "Chillwave pork belly try-hard ennui organic chia. Occupy polaroid seitan brunch master cardigan tote bag tofu. Shabby chic kale chips pop-up thundercats beard.",
      "image": "",
      "createdAt": 149511973000
    },
    // ...
  ]
}
```

## Examples

{% method %}
### GET /fundraising-events/35/incentives
Returns the incentives for the fundraising event with an ID of 35.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/fundraising-events/35/incentives
```

{% sample lang="js" %}
```js
try {
  const incentives = await Tiltify.FundraisingEvent.incentives(35)
  // do something with the incentives
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  incentives = Tiltify::FundraisingEvent.incentives(35)
  # do something with the incentives
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.FundraisingEvent.incentives(35) do
  {:ok, incentives} -> # do something with the incentives
  {:error, error} -> # handle error
end
```

{% endmethod %}
