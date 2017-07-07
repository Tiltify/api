# GET /polls

Returns a list of polls on Tiltify. This is a paginated endpoint.

```js
{
  "meta": {
    "status": 200
  },
  "data": [
    {  
      "id": 47,
      "name": "Should pineapple go on pizza?",
      "active": true,
      "campaignId": 1337,
      "createdAt": 1498169329000,
      "options":[  
        {  
          "name":"No",
          "amount": 9001,
          "percentage": 100
        },
        {  
          "name":"Yes",
          "amount": 0,
          "percentage": 0
        },
      ]
    },
    {
      // ...
    }
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
### GET /polls
Returns a list of the first 100 polls by default

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/polls
```

{% sample lang="js" %}
```js
try {
  const polls = await Tiltify.Poll.index()
  // do something with the polls
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  polls = Tiltify::Poll.index()
  # do something with the polls
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Poll.index() do
  {:ok, polls} -> # do something with the polls
  {:error, error} -> # handle error
end
```

{% endmethod %}
