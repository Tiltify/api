# GET /user

Returns the currently authenticated user.
If no user is authenticated, this will return not authorized.

```js
{
  "meta": {
    "status": 200
  },
  "data": {
    "id": 3,
    "username": "TiltifyUser",
    "slug": "tiltify-user",
    "thumbnail": "https://asdfasdfasdf.cloudfront.net/1234.jpg",
    "status": "completed"
  }
}
```

## Examples

{% method %}
### GET /user
Returns the currently authenticated user.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/user
```

{% sample lang="js" %}
```js
try {
  const user = await Tiltify.User.current()
  // do something with the users
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  user = Tiltify::User.current()
  # do something with the user
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.User.current() do
  {:ok, user} -> # do something with the user
  {:error, error} -> # handle error
end
```

{% endmethod %}
