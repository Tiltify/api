# GET /fundraising-events/:id/incentives

Endpoint to retrieve the incentives for a fundraising event.

```js
{
  "meta": {
    "status": 200
  },
  "data": [
    {
      "id": 1,
      "title": "A Special Incentive for the streamers",
      "description": "Chillwave pork belly try-hard ennui organic chia. Occupy polaroid seitan brunch master cardigan tote bag tofu. Shabby chic kale chips pop-up thundercats beard.",
      "image": {
        "src": "https://asdf.cloudfront.net/asdf.jpg",
        "alt": "synthesize distributed solutions",
        "width": 200,
        "height": 200
      },
      "createdAt": 149511973000
    },
    // ...
  ]
}
```

## Examples

{% method %}
### GET /fundraising-events/35/incentives
Returns the incentives for the fundraising event with an ID of 35.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/fundraising-events/35/incentives
```

{% endmethod %}
