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
  "createdAt": 1498232189000,
  "updatedAt": 1498232189000
}
```

## Fields

|key|description|
|:---|:---|
|**id**<br>integer| This is the id of the challenge.
|**name**<br>string| The name of the challenge.
|**amount**<br>currency| The amount of money required to raise to complete this challenge.
|**totalAmountRaised**<br>currency| The amount of money currently raised by this challenge.
|**active**<br>boolean| Whether or not the challenge is active.
|**campaignId**<br>integer| The campaign this challenge is associated to.
|**endsAt**<br>date| When the challenge ends.
|**createdAt**<br>date| Date of challenge creation.
|**updatedAt**<br>date| Date of last challenge update.
