# Challenge

A challenge is an incentive for a campaign.

```js
{
  "id": 466,
  "name": "Bounty hunters! We don't need this scum.",
  "amount": 91,
  "totalAmountRaised": 186,
  "active": true,
  "activatesOn": 1498169329000,
  "campaignId": 231,
  "endsAt": 1505762373000,
  "createdAt": 1498232189000
}
```

## Fields

|key|description|
|:---|:---|
|**id**<br>integer| This is the id of the challenge.
|**name**<br>string| The name of the challenge.
|**amount**<br>integer| The amount in total donations required to complete the challenge.
|**totalAmountRaised**<br>integer| The amount raised for the challenge so far.
|**active**<br>boolean| Whether or not the challenge is currently active.
|**activatesOn**<br>date| Date of challenge creation.
|**campaignId**<br>integer| The campaign this challenge is associated to.
|**endsAt**<br>date| The ending time for the challenge
|**createdAt**<br>date| Date of challenge creation.
