>### Deprecation Notice
>Api V3 is being deprecated on July 1st, 2023. Please consider updating to V5

>[V5 Api Documentation](https://v5api.tiltify.com/api/public)

-----

# GET /causes/:id/leaderboards

If the cause has allowed global leaderboards to be visible this endpoint will
return said leaderboards with up to 25 entries per.

```js

{
  "meta": {
    "status": 200
  },
  "data": {
    "individual": [
      {
        "userId": 2494,
        "name": "iKasperr",
        "url": "https://tiltify.com/@ikasperr",
        "amount_raised": 128930
      },
      // ...
    ],
    "team": [
      {
        "teamId": 387,
        "name": "DerpSquad",
        "url": "https://tiltify.com/+derpsquad",
        "amount_raised": 50493
      },
      // ...
    ],
  }
}
```

## Examples

{% method %}
### GET /causes/35/leaderboards
Returns a single campaign entity with the ID of 42.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/causes/35/leaderboards
```

{% endmethod %}
