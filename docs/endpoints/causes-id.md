>### Deprecation Notice
>Api V3 is being deprecated on July 1st, 2023. Please consider updating to V5

>[V5 Api Documentation](https://v5api.tiltify.com/api/public)

-----

# GET /causes/:id

Retreives a single cause given an identifier.

```js
{
  "meta": {
    "status": 200
  },
  "data": {
    "id": 35,
    "name": "Good Cause",
    "legalName": "Good Cause Inc",
    "slug": "goodcause",
    "currency": "USD",
    "about": "We do good stuff",
    "video": "https://www.youtube.com/watch?v=dQw4w9WgXcQ",
    "image": {
      "src": "https://asdf.cloudfront.net/asdf.jpg",
      "alt": "",
      "width": 640,
      "height": 360
    },
    "avatar": {
      "src": "https://asdf.cloudfront.net/asdf.jpg",
      "alt": "",
      "width": 64,
      "height": 64
    },
    "logo": {
      "src": "https://asdf.cloudfront.net/asdf.jpg",
      "alt": "",
      "width": 100,
      "height": 64
    },
    "banner": {
      "src": "https://asdf.cloudfront.net/asdf.jpg",
      "alt": "",
      "width": 530,
      "height": 1440
    },
    "contactEmail": "asdf@example.org",
    "paypalEmail": "asdf@example.org",
    "paypalCurrencyCode": "USD",
    "social": {
      "twitter": "stjude",
      "youtube": "",
      "facebook": "stjude",
      "instagram": "stjude"
    },
    "settings": {
      "colors": {
        "background": "#fff",
        "highlight": "#ce2f40"
      },
      "headerIntro": "Start a fundraising campaign to help us do good things.",
      "headerTitle": "Good Cause",
      "footerCopyright": "© Copyright 2017. Good Cause Inc",
      "findOutMoreLink": "https://www.example.com/find-out-more"
    },
    "status": "published",
    "stripeConnected": true,
    "mailchimpConnected": false,
    "address": {
      "addressLine1": "123 Some St",
      "addressLine2": "",
      "city": "Houston",
      "region": "TX",
      "postalCode": "77008",
      "country": "US"
    }
  }
}
```

## Examples

{% method %}
### GET /causes/42
Returns a single cause entity with the ID of 42.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/causes/42
```

{% endmethod %}

---

{% method %}
### GET /cause/cause-slug
Returns a single cause entity with a slug of cause-slug.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/causes/cause-slug
```

{% endmethod %}
