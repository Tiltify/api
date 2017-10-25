# /fundraising-events/:id/visibility-options

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
    "startsAt": {
      "visible": true
    },
    "endsAt": {
      "visible": true
    },
    "fundraiserGoalAmount": {
      "visible": true,
      "type": "BOTH"
    },
    "individualLeaderboard": {
      "visible": true
    },
    "teamLeaderboard": {
      "visible": true,
      "type": "ALL"
    },
    "donorLeaderboard": {
      "visible": true,
      "type": "ALL"
    },
    "preventDonationsBeforeStart": {
      "visible": false
    },
    "registration": {
      "visible": false
    },
    "donate": {
      "visible": true
    }
  }
}
```

## Examples

{% method %}
### GET /fundraising-events/35/visibility-options
Returns visibility options for a fundraising event with the ID of 35

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/fundraising-events/35/visibility-options
```

{% endmethod %}
