# /fundraising-events

Retrieves a paginated array of 100 Fundraising Events by default

```js
{
  "meta": {
    "status": 200
  },
  "data": [
    {
      "id": 1,
      "name": "Big Event 2017",
      "slug": "big-event-2017",
      "url": "https://tiltify.com/cause-slug/big-event-2017",
      "description": "Play For More Than Bragging Rights\r\n\r\nSign up to create your own campaign and start fundraising. Play and stream your favorite video games to raise donations and unlock exclusive loot.\r\n\r\nSt. Jude has helped push the childhood cancer survival rate from less than 20% when we opened to 80% today. We won’t stop until no child dies from cancer.",
      "video": "https://www.youtube.com/watch?v=e-ORhEE9VVg",
      "image": "https://asdfasdfasdf.cloudfront.net/1234.jpg",
      "logo": "https://asdfasdfasdf.cloudfront.net/1234.jpg",
      "avatar": "https://asdfasdfasdf.cloudfront.net/1234.jpg",
      "bannerSrc": "https://asdfasdfasdf.cloudfront.net/1234.jpg",
      "bannerAlt": "Some text describing the banner image",
      "bannerTitle": "St. Jude PLAY LIVE",
      "bannerIntro": "Play video games and create a fundraising campaign to help kids battling cancer.",
      "currency": "USD",
      "goal": 10000,
      "amountRaised": 8923,
      "startsOn": "2017-03-24",
      "endsOn": "2017-03-26",
      "causeId": 17
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
### GET /fundraising-events
Returns a list of the first 100 Fundraising Events by default

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/fundraising-events
```

{% sample lang="js" %}
```js
try {
  const fundraisingEvent = await Tiltify.FundraisingEvent.index()
  // do something with the fundraising events
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  fundraising_event = Tiltify::FundraisingEvent.index()
  # do something with the fundraising events
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.FundraisingEvent.index() do
  {:ok, fundraising_event} -> # do something with the fundraising events
  {:error, error} -> # handle error
end
```

{% endmethod %}
