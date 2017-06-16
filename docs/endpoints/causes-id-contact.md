# /causes/:id/contact

Retrieves the publically available contact information for a cause.

```js
{
  "legalName": "Good Cause Inc.",
  "email": "dev@tiltify.com",
  "twitter": "tiltify",
  "youtube": "tiltify",
  "facebook": "tiltify",
  "instagram": "tiltify",
  "snapchat": "tiltify",
  "address": {
    "addressLine1": "123 Some St",
    "addressLine2": "",
    "city": "Houston",
    "region": "TX",
    "postalCode": "77008",
    "country": "US"
  }
}
```

## Examples

{% method %}
### GET /causes/35/contact
Returns the contact information for a given cause

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/causes/35/contact
```

{% sample lang="js" %}
```js
try {
  const contact = await Tiltify.Cause.contact(35)
  // do something with the contact information
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  contact = Tiltify::Cause.contact(35)
  # do something with the contact
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Cause.contact(35) do
  {:ok, contact} -> # do something with the contact
  {:error, error} -> # handle error
end
```

{% endmethod %}
