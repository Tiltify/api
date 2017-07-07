# GET /polls/:id

Retrieves a single poll given an identifier.

```js
{
  "meta": {
    "status": 200
  },
  "data": {
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
      }
    ]
  }
}
```

## Examples

{% method %}
### GET /polls/387
Returns a single poll entity with the ID of 387.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/polls/387
```

{% sample lang="js" %}
```js
try {
  const poll = await Tiltify.Poll.get(387)
  // do something with the poll
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  poll = Tiltify::Poll.get(387)
  # do something with the poll
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Poll.get(387) do
  {:ok, poll} -> # do something with the poll
  {:error, error} -> # handle error
end
```

{% endmethod %}
