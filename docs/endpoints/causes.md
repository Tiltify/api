# GET /causes

Returns a list of causes on Tiltify. This is a paginated endpoint.

```js
[
  {
    // ... Cause fields
  },
  // ... Additional causes
]
```

## Examples

{% method %}
### GET /causes
Returns a list of the first 100 causes by default

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/causes
```

{% sample lang="js" %}
```js
try {
  const causes = await Tiltify.Cause.index()
  // do something with the causes
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  causes = Tiltify::Cause.index()
  # do something with the causes
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Cause.index() do
  {:ok, causes} -> # do something with the causes
  {:error, error} -> # handle error
end
```

{% endmethod %}
