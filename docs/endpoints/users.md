# GET /users

Returns a list of users on Tiltify. This is a paginated endpoint.

```js
{
  "meta": {
    "status": 200
  },
  "data": [
    {
      "id": 3,
      "username": "TiltifyUser",
      "slug": "tiltify-user",
      "thumbnail": {
        "src": "https://asdf.cloudfront.net/asdf.jpg",
        "alt": "synthesize distributed solutions",
        "width": 200,
        "height": 200
      },
      "status": "completed"
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
### GET /users
Returns a list of the first 100 users by default

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/users
```

{% endmethod %}
