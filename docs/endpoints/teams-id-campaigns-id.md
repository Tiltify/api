# GET /teams/:id/campaigns/:id

Retrieves a single campaign given a team and campaign identifier. This resource
allows routing by slug.

```js
{
  "meta": {
    "status": 200
  },
  "data": {
    "id": 1,
    "name": "My Awesome Campaign",
    "slug": "my-awesome-campaign",
    "url": "/@username/my-awesome-campaign",
    "startsAt": 1493355600000,
    "endsAt": 1496206800000,
    "description": "My awesome weekend campaign.",
    "avatar": {
      "src": "https://asdf.cloudfront.net/asdf.jpg",
      "alt": "",
      "width": 200,
      "height": 200
    },
    "causeId": 17,
    "fundraisingEventId": 39,
    "fundraiserGoalAmount": 10000,
    "originalGoalAmount": 5000,
    "amountRaised": 3402.00,
    "supportingAmountRaised": 8923.00,
    "totalAmountRaised": 12325.00,
    "supportable": true,
    "status": "published",
    "user": {
      "id": 1,
      "username": "UserName",
      "slug": "username",
      "url": "/@username",
      "avatar": {
        "src": "https://asdf.cloudfront.net/asdf.jpg",
        "alt": "",
        "width": 200,
        "height": 200
      }
    },
    "team": {
      "id": 1,
      "username": "Team Name",
      "slug": "teamslug",
      "url": "/+teamslug",
      "avatar": {
        "src": "https://asdf.cloudfront.net/asdf.jpg",
        "alt": "",
        "width": 200,
        "height": 200
      }
    },
    "livestream": {
      "type": "twitch",
      "channel": "tiltify"
    }
  }
}
```

## Examples

{% method %}
### GET /teams/1/campaigns/42
Returns a single campaign entity with the ID of 42 and a user ID of 1

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/teams/1/campaigns/42
```

{% endmethod %}

{% method %}
### GET /teams/teamerino/campaigns/campaign-slug
Returns a single campaign entity with the slug of campaign-slug and a username
of teamerino

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/users/teamerino/campaigns/campaign-slug
```

{% endmethod %}

---
