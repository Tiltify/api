# GET /campaigns

Retrieves the most recent campaigns in descending order

---

|Attributes||
|:---|:---|
|**count**<br>integer| This is the total amount of requested records.<br>Default: 100 <br>Min: 1<br>Max: 100<br>(optional)|
|**after**<br>integer| This is the last id from the previous record set.<br><i>This is important because some records may be deleted, and it lets you reference the last record sets id directly</i><br>(optional)|
|**before**<br>integer| This is the first id from the current record set.<br>(optional)|

```js
{
  "meta": {
    "status": 200
  },
  "data": [
    {
      "id": 1234,
      "name": "My Awesome Campaign",
      "slug": "my-awesome-campaign",
      "url": "https://tiltify.com/@username/my-awesome-campaign",
      "description": "My awesome weekend campaign.",
      "thumbnail": {
        "src": "https://asdf.cloudfront.net/asdf.jpg",
        "alt": "synthesize distributed solutions",
        "width": 200,
        "height": 200
      },
      "causeId": 17,
      "userId": 14,
      "teamId": null,
      "fundraisingEventId": 39,
      "goal": 10000,
      "originalGoal": 5000,
      "amountRaised": 8923,
      "totalAmountRaised": 12325,
      "startsOn": "2017-03-24",
      "endsOn": "2017-03-26"
    },
    // ...
  ],
  "links": {
    "next": "/api/v3/campaigns?after=1232",
    "prev": "/api/v3/campaigns?before=1233",
    "self": "/api/v3/campaigns"
    "first": "/api/v3/campaigns"
    "last": "/api/v3/campaigns?after=0"
  }
}
```

## Examples

{% method %}
### GET /campaigns
Returns the last 100 campaign entities.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/campaigns
```

{% sample lang="js" %}
```js
try {
  const campaign = await Tiltify.Campaign.list()
  // do something with the campaign
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  campaign = Tiltify::Campaign.list()
  # do something with the campaign
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Campaign.list() do
  {:ok, campaigns} -> # do something with the campaign
  {:error, error} -> # handle error
end
```

{% endmethod %}

{% method %}
### GET /campaigns?count=50
Returns the last 50 campaign entities.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/campaigns?count=50
```

{% sample lang="js" %}
```js
const options = {
  count: 50
}

try {
  const campaign = await Tiltify.Campaign.list(options)
  // do something with the campaign
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  campaign = Tiltify::Campaign.list(count: 50)
  # do something with the campaign
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Campaign.list(count: 50) do
  {:ok, campaigns} -> # do something with the campaign
  {:error, error} -> # handle error
end
```

{% endmethod %}
