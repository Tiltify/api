# GET /user

Returns the currently authenticated user.
If no user is authenticated, this will return not authorized.

```js
{
  "meta": {
    "status": 200
  },
  "data": {
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
  }
}
```

## Examples

{% method %}
### GET /user
Returns the currently authenticated user.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/user
```

{% endmethod %}
