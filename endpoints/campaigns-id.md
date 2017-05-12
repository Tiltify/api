# GET /campaigns/:id

Retreives a single campaign given an identifier.

```json
{
  "id": 1,
  "name": "My Awesome Campaign",
  "slug": "my-awesome-campaign",
  "url": "/@username/my-awesome-campaign",
  "description": "My awesome weekend campaign.",
  "thumbnail": "https://asdfasdfasdf.cloudfront.net/1234.jpg",
  "causeId": 17,
  "userId": 14,
  "teamId": null,
  "fundraisingEventId": 39,
  "goal": 10000,
  "originalGoal": 5000,
  "amountRaised": 8923,
  "totalAmountRaised": 12325,
  "startsOn": "2017-03-24",
  "endsOn": "2017-03-26"
}
```

## Examples

##### GET /campaigns/42
Returns a single campaign entity with the ID of 42.

##### GET /campaigns/campaign-slug
Returns a single campaign entity with a slug of campaign-slug. Note that it
will pull the first campaign found with this slug. This is typically not the
expected result and you should instead pass a reference to a user

##### GET /campaigns/campaign-slug?username=ben
Returns a single campaign entity with a slug of campaign-slug belonging to the
user with a username of ben.

##### GET /campaigns/campaign-slug?user_id=37
Returns a single campaign entity with a slug of campaign-slug belonging to the
user with an id of 37
