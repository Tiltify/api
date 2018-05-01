# GET /users/:id/teams

Returns an array of teams a user belongs to

```js
{
  "meta": {
    "status": 200
  },
  "data": [
    {
      "id": 958,
      "name": "Chive Charities (Mock-Up for Demo)",
      "slug": "chive-charities-mock-up-for-demo",
      "url": "https://tiltify.com/+chive-charities-mock-up-for-demo",
      "avatar": {
        "alt": "",
        "height": 200,
        "src": "https://asdf.cloudfront.net/asdf.jpg",
        "width": 200,
      }
    },
    // ...
  ]
}
```

## Examples

{% method %}
### GET /users/1/teams
Returns an array of teams a user belongs to

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/users/1/teams
```
{% endmethod %}
