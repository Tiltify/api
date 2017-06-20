# GET /fundraising-events/:id/registration-fields

Returns an object describing the registration fields for a fundraising event.

```js
{
  "meta": {
    "status": 200
  },
  "data": {
    "address": {
      "enabled": true
    },
    "shirt_size": {
      "enabled": true
    },
    "service_hours": {
      "enabled": true
    }
  }
}
```

## Examples

{% method %}
### GET /fundraising-events/1/registration-fields
Returns the registration field settings for a fundraising event with an id of 1.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/fundraising-events/1/registration-fields
```

{% sample lang="js" %}
```js
try {
  const registrationFields = await Tiltify.FundraisingEvent.registrationFields(1)
  // do something with the registrationFields
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  registration_fields = Tiltify::FundraisingEvent.registration_fields(1)
  # do something with the registration_fields
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.FundraisingEvent.registration_fields(1) do
  {:ok, registration_fields} -> # do something with the registration_fields
  {:error, error} -> # handle error
end
```

{% endmethod %}
