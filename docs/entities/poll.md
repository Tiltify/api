# Poll

A poll is an incentive for a campaign.

```js
{  
  "id": 47,
  "name": "Should pineapple go on pizza?",
  "active": true,
  "campaignId": 1337,
  "createdAt": 1498169329000,
  "options":[  
    {  
      "name":"No",
      "amount": 9001,
      "percentage": 100
    },
    {  
      "name":"Yes",
      "amount": 0,
      "percentage": 0
    },
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
|**options**<br>array| Array of poll options.

## Poll Option Fields

|key|description|
|:---|:---|
|**name**<br>string| The name of the poll option.
|**amount**<br>integer| The total amount raised under the poll option.
|**percentage**<br>float| The percentage of the amount the option has raised.
