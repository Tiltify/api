>### Deprecation Notice
>Api V3 is being deprecated on July 1st, 2023. Please consider updating to V5

>[V5 Api Documentation](https://v5api.tiltify.com/api/public)

-----

# GET /users/:id

Retrieves a specific user by ID or slug

```js
{
  "meta": {
    "status": 200
  },
  "data": {
    "id": 3,
    "username": "TiltifyUser",
    "slug": "tiltify-user",
    "url": "https://tiltify.com/@tiltify-user"
    "avatar": {
      "src": "https://asdf.cloudfront.net/asdf.jpg",
      "alt": "",
      "width": 200,
      "height": 200
    },
    "about": "I'm the best",
    "totalAmountRaised": 1234.23,
    "social": {
      "facebook": null,
      "twitch": "tiltify",
      "twitter": null,
      "website": null,
      "youtube": null,
    }
  }
}
```
