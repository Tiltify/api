# GET /causes/:id/donations

Authenticated and paginated endpoint to retrieve the donations for a cause.

```js
[
  {
    "id": 1,
    "amount": 5.0,
    "name": "Tiltify Devs",
    "email": "dev@tiltify.ccom",
    "method": "paypal",
    "transactionId": "2CH1234123412341234",
    "donatedAt": "2017-04-01T00:00:00+00:00",
    "donatableId": 123,
    "causeId": 42,
    "userId": null,
    "donatableType": "Campaign"
  },
  // ...
]
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
