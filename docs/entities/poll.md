>### Deprecation Notice
>Api V3 is being deprecated on July 1st, 2023. Please consider updating to V5

>[V5 Api Documentation](https://v5api.tiltify.com/api/public)

-----

# Poll

A poll is an incentive for a campaign.

```js
{
  "id": 47,
  "name": "Should pineapple go on pizza?",
  "active": true,
  "campaignId": 1337,
  "createdAt": 1498169329000,
  "updatedAt": 1498169329000,
  "options":[
    {
      "id": 42,
      "pollId": 47,
      "name":"No",
      "totalAmountRaised": 50,
      "createdAt": 1498169329000,
      "updatedAt": 1498169329000
    },
    {
      "id": 44,
      "pollId": 47,
      "name":"Yes",
      "totalAmountRaised": 50,
      "createdAt": 1498169329000,
      "updatedAt": 1498169329000
    }
  ]
}
```

## Fields

|key|description|
|:---|:---|
|**id**<br>integer| This is the id of the poll.
|**name**<br>string| The name of the poll.
|**active**<br>boolean| Whether or not the poll is active.
|**campaignId**<br>integer| The campaign this poll is associated to.
|**createdAt**<br>date| Date of poll creation.
|**updatedAt**<br>date| Date of last poll update.
|**options**<br>array| Array of poll options.

## Poll Option Fields

|key|description|
|:---|:---|
|**id**<br>integer| The id of the poll option.
|**pollId**<br>integer| The id of poll this option belongs to.
|**name**<br>string| The name of the poll option.
|**totalAmountRaised**<br>integer| The total amount raised under the poll option.
|**createdAt**<br>date| Date of poll option creation.
|**updatedAt**<br>date| Date of last poll option update.
