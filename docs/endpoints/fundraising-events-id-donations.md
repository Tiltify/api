# GET /fundraising-events/:id/donations

Authenticated and paginated endpoint to retrieve the donations for a fundraising-event.

```js
{
  "meta": {
    "status": 200
  },
  "data": [
    {
      "id": 21347,
      "amount": 556.0,
      "name": "Yoda",
      "donorComment": "Judge me by my size, do you?",
      "createdAt": 1490328000000
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
### GET /fundraising-events/35/donations
Returns the donations for the fundraising event with an ID of 35.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/fundraising-events/35/donations
```

{% sample lang="js" %}
```js
try {
  const donations = await Tiltify.FundraisingEvent.donations(35)
  // do something with the donations
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  donations = Tiltify::FundraisingEvent.donations(35)
  # do something with the donations
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.FundraisingEvent.donations(35) do
  {:ok, donations} -> # do something with the donations
  {:error, error} -> # handle error
end
```

{% endmethod %}
