>### Deprecation Notice
>Api V3 is being deprecated on July 1st, 2023. Please consider updating to V5

>[V5 Api Documentation](https://v5api.tiltify.com/api/public)

-----

# /causes/:id/visibility-options

Retrieves and updates the visibility options for a cause. These options are
used to determine the visibility of certain features on the frontend of the
website. These options also disable features in the API such as whether or not
a user can donate directly to a cause, or whether the leaderboards are
publically available.

```js
{
  "meta": {
    "status": 200
  },
  "data": {
    "donate": {
      "visible": true
    },
    "individual_leaderboard": {
      "visible": true,
      "type": "ALL"
    },
    "team_leaderboard": {
      "visible": true,
      "type": "ALL"
    }
  }
}
```

## Examples

{% method %}
### GET /causes/35/visibility-options
Returns a single campaign entity with the ID of 42.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/causes/35/visibility-options
```
{% endmethod %}

---

{% method %}
### PATCH /causes/35/visibility-options
Update the visibility of the donate button on the cause page for the cause with
id of 35.

{% sample lang="curl" %}
```bash
curl -X PATCH \
  -H 'Content-Type: application/json' \
  -d '{"donate": { "visible": false }}' \
  https://tiltify.com/api/v3/causes/35/visibility-options
```

{% endmethod %}
