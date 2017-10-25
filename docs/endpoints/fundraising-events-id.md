# /fundraising-events/:id

Retrieves a single entity of a Fundraising Event

```js
{
  "meta": {
    "status": 200
  },
  "data": {
    "id": 34,
    "name": "Big Event 2017",
    "slug": "big-event-2017",
    "url": "https://tiltify.com/cause-slug/big-event-2017",
    "description": "Play For More Than Bragging Rights\r\n\r\nSign up to create your own campaign and start fundraising. Play and stream your favorite video games to raise donations and unlock exclusive loot.\r\n\r\nSt. Jude has helped push the childhood cancer survival rate from less than 20% when we opened to 80% today. We won’t stop until no child dies from cancer.",
    "video": {
      "src": "https://www.youtube.com/watch?v=dQw4w9WgXcQ",
      "alt": "synthesize distributed solutions",
      "width": 640,
      "height": 360
    },
    "image": {
      "src": "https://asdf.cloudfront.net/asdf.jpg",
      "alt": "synthesize distributed solutions",
      "width": 640,
      "height": 360
    },
    "avatar": {
      "src": "https://asdf.cloudfront.net/asdf.jpg",
      "alt": "synthesize distributed solutions",
      "width": 64,
      "height": 64
    },
    "logo": {
      "src": "https://asdf.cloudfront.net/asdf.jpg",
      "alt": "synthesize distributed solutions",
      "width": 64,
      "height": 100
    },
    "banner": {
      "src": "https://asdf.cloudfront.net/asdf.jpg",
      "alt": "synthesize distributed solutions",
      "width": 530,
      "height": 1440
    },
    "bannerTitle": "St. Jude PLAY LIVE",
    "bannerIntro": "Play video games and create a fundraising campaign to help kids battling cancer.",
    "currency": "USD",
    "goal": 10000,
    "amountRaised": 8923,
    "startsOn": "2017-03-24",
    "endsOn": "2017-03-26",
    "causeId": 17
  }
}
```

## Examples

{% method %}
### GET /fundraising-events/34
Retrieves a single entity of a Fundraising Event with the ID of 34

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/fundraising-events/34
```

{% endmethod %}
