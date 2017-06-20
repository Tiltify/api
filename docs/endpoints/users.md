# GET /users

Returns a list of users on Tiltify. This is a paginated endpoint.

```js
{
  "meta": {
    "status": 200
  },
  "data": [
    {
      "id": 3,
      "username": "TiltifyUser",
      "slug": "tiltify-user",
      "thumbnail": "https://asdfasdfasdf.cloudfront.net/1234.jpg",
      "status": "completed"
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
### GET /users
Returns a list of the first 100 users by default

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/users
```

{% sample lang="js" %}
```js
try {
  const users = await Tiltify.User.index()
  // do something with the users
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  users = Tiltify::User.index()
  # do something with the users
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.User.index() do
  {:ok, users} -> # do something with the users
  {:error, error} -> # handle error
end
```

{% endmethod %}
