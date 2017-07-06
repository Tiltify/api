# Reward

A reward is an incentive for a campaign.

```js
{
  "id": 1,
  "alwaysActive": true,
  "name": "Fingerstache vhs paleo tattooed echo cold-pressed.",
  "amount": 43,
  "kind": "virtual",
  "quantity": null,
  "remaining": null,
  "fairMarketValue": 88,
  "startsAt": null,
  "endsAt": 1511264923000,
  "description": "Chuck Norris can access the DB from the UI.",
  "shippingAddressRequired": false,
  "shippingNote": null,
  "image": {
    "src": "",
    "alt": "Chuck Norris can access the DB from the UI.",
    "width": 200,
    "height": 200
  },
  "currency": "USD",
  "createdAt": 1498169329000
}
```

## Fields

|key|description|
|:---|:---|
|**id**<br>integer| This is the id of the reward.
|**alwaysActive**<br>boolean| Whether or not the reward is always active.
|**name**<br>string| The name of the reward.
|**amount**<br>integer| The required donation amount for the reward.
|**kind**<br>string| The type of reward. <br> (Product, Virtual, or Physical)
|**quantity**<br>integer| The quantity of rewards available.
|**remaining**<br>integer| The quantity of rewards remaining.
|**fairMarketValue**<br>integer| The fair market value of the reward.
|**startsAt**<br>date| When the reward unlocks.<br>(Only if <strong>alwaysActive</strong> is ```false```)
|**endsAt**<br>date| When the reward is removed from availability.<br>(Only if <strong>alwaysActive</strong> is ```false```)
|**description**<br>md-string| The description of the campaign in markdown format. We support basic markdown functionality, so any common markdown should work.
|**shippingAddressRequired**<br>boolean| Denotes if a reward requires shipping information.
|**shippingNote**<br>string| Customized note related to shipping.
|**image**<br>image| An image object for the reward.
|**currency**<br>string| The currency the reward is in.
|**createdAt**<br>date| Date of reward creation.
