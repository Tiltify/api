>### Deprecation Notice
>Api V3 is being deprecated on July 1st, 2023. Please consider updating to V5

>[V5 Api Documentation](https://v5api.tiltify.com/api/public)

-----

# GET /fundraising-events/:id/registration-fields

Returns an object describing the registration fields for a fundraising event.

```js
{
  "meta": {
    "status": 200
  },
  "data": {
    "address": {
      "enabled": true
    },
    "shirt_size": {
      "enabled": true
    },
    "service_hours": {
      "enabled": true
    }
  }
}
```

## Examples

{% method %}
### GET /fundraising-events/1/registration-fields
Returns the registration field settings for a fundraising event with an id of 1.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/fundraising-events/1/registration-fields
```

{% endmethod %}
