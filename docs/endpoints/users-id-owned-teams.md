>### Deprecation Notice
>Api V3 is being deprecated on July 1st, 2023. Please consider updating to V5

>[V5 Api Documentation](https://v5api.tiltify.com/api/public)

-----

# GET /users/:id/owned-teams

Retrieves the teams owned by a specific user.

```js
{
  "meta": {
    "status": 200
  },
  "data": [
    {
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
    },
    // ...
  ]
}
```
