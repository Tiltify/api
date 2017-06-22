# GET /causes

Returns a list of causes on Tiltify. This is a paginated endpoint.

```js
{
  "meta": {
    "status": 200
  },
  "data": [
    {
      "id": 3,
      "slug": "hickle-emard-and-keeling-cause",
      "name": "Hickle, Emard and Keeling Cause",
      "legalName": "Hickle, Emard and Keeling Charity",
      "about": "Food truck artisan scenester migas health authentic williamsburg. Chillwave pinterest thundercats retro yolo. Sartorial thundercats five dollar toast venmo pbr&b. Asymmetrical microdosing bicycle rights.",
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
      "contactEmail": "francesca.goldner@ortizerdman.co",
      "paypalEmail": "test@cause.com",
      "paypalCurrencyCode": "USD",
      "totalAmountRaised": 76154,
      "social": {},
      "settings": {
        "colors": {
          "background": "#fff",
          "highlight": "#ce2f40"
        },
        "visibilityOptions": {
          "teamLeaderboard": {
            "visible": true,
            "type": "ALL"
          },
          "individualLeaderboard": {
            "visible": true,
            "type": "ALL"
          },
          "donate": {
            "visible": true
          }
        },
        "social": null
      },
      "status": "published",
      "stripeConnected": false,
      "mailchimpConnected": false,
      "address": {
        "addressLine1": "454 Orval Springs",
        "addressLine2": "Suite 181",
        "city": "East Loufort",
        "region": "Mississippi",
        "postalCode": "93355",
        "country": "Gibraltar"
      }
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
