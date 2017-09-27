# Reward

A reward is an incentive for a campaign.

```js
{
  "id": 1,
  "name": "Fingerstache vhs paleo tattooed echo cold-pressed.",
  "description": "Chuck Norris can access the DB from the UI.",
  "amount": 43,
  "kind": "virtual",
  "quantity": null,
  "remaining": null,
  "fairMarketValue": 88,
  "currency": "USD",
  "shippingAddressRequired": false,
  "shippingNote": null,
  "image": {
    "src": "",
    "alt": "Chuck Norris can access the DB from the UI.",
    "width": 270,
    "height": 176
  },
  "active": true,
  "startsAt": 0,
  "createdAt": 1498169329000,
  "updatedAt": 1498249889000
}
```

## Fields

|key|description|
|:---|:---|
|**id**<br>integer| This is the id of the reward.
|**name**<br>string| The name of the reward.
|**description**<br>md-string| The description of the reward in markdown format.
|**amount**<br>integer| The required donation amount for the reward.
|**kind**<br>string| The type of reward. <br> (product, virtual, or physical)
|**quantity**<br>integer| The quantity of rewards available.
|**remaining**<br>integer| The quantity of rewards remaining.
|**fairMarketValue**<br>integer| The fair market value of the reward.
|**currency**<br>string| The currency the reward is in.
|**shippingAddressRequired**<br>boolean| Denotes if a reward requires shipping information.
|**shippingNote**<br>string| Customized note related to shipping.
|**image**<br>image| An image object for the reward.
|**active**<br>boolean| Whether the reward is toggled to be visible.
|**startsAt**<br>date| When the reward unlocks.
|**createdAt**<br>date| Date of reward creation.
|**updatedAt**<br>date| Date of last change to reward data.
