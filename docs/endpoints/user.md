>### Deprecation Notice
>Api V3 is being deprecated on July 1st, 2023. Please consider updating to V5

>[V5 Api Documentation](https://v5api.tiltify.com/api/public)

-----

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
