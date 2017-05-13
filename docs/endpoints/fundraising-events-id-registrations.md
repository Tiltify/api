# GET /fundraising-events/:id/registrations

This is an authorization required endpoint which returns the registrations made
to a specific fundraising event.

```js
[
  {
    "id": 4,
    "userId": 9444,
    "email": "dev@tiltify.com",
    "subscribed": true,
    "registeredAt": "2017-04-07T12:10:16.364-04:00",
    "address": {
      "addressLine1": "123 Over there",
      "addressLine2": "#123",
      "city": "Houston",
      "state": "TX",
      "postalCode": "12345",
    },
    "shirtSize": "M",
    "serviceHours": false
  },
  // ... additional registrations
]
```

## Examples

{% method %}
### GET /fundraising-events/1/registrations
Returns the registration field settings for a fundraising event with an id of 1.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/fundraising-events/1/registrations
```

{% sample lang="js" %}
```js
try {
  const registrations = await Tiltify.FundraisingEvent.registrations(1)
  // do something with the registrations
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  registrations = Tiltify::FundraisingEvent.registrations(1)
  # do something with the registrations
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.FundraisingEvent.registrations(1) do
  {:ok, registrations} -> # do something with the registrations
  {:error, error} -> # handle error
end
```

{% endmethod %}
