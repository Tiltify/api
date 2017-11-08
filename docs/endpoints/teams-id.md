# GET /teams/:id

Retreives a single team given an identifier.

```js
{
  "meta": {
    "status": 200
  },
  "data": {
    "id": 387,
    "name": "DerpSquad",
    "slug": "derpsquad",
    "url": "https://tiltify.com/+derpsquad",
    "bio": "",
    "inviteOnly": true,
    "disbanded": false,
    "social": {
      "facebook": "tradechatonyoutube",
      "twitch": "tradechat",
      "twitter": "tradechat",
      "website": "",
      "youtube": "tradechat"
    },
    "avatar": {
      "src": "https://asdf.cloudfront.net/asdf.jpg",
      "alt": "",
      "width": 200,
      "height": 200
    }
  }
}
```

## Examples

{% method %}
### GET /teams/387
Returns a single team entity with the ID of 387.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/teams/387
```
{% endmethod %}

---

{% method %}
### GET /teams/derpsquad
Returns a single team entity with a slug of derpsquad.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/teams/derpsquad
```

{% endmethod %}
