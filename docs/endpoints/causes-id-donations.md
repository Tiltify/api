# GET /causes/:id/donations

Authenticated and paginated endpoint to retrieve the donations for a cause.

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
### GET /causes/35/donations
Returns the donations for the cause with an ID of 35.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/causes/35/donations
```

{% sample lang="js" %}
```js
try {
  const donations = await Tiltify.Cause.donations(35)
  // do something with the donations
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  donations = Tiltify::Cause.donations(35)
  # do something with the donations
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Cause.donations(35) do
  {:ok, donations} -> # do something with the donations
  {:error, error} -> # handle error
end
```

{% endmethod %}
