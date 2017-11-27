# Campaigns

A campaign is the event you create to fundraise for your favorite cause.

```js
{
  "id": 1,
  "name": "My Awesome Campaign",
  "slug": "my-awesome-campaign",
  "url": "https://tiltify.com/@username/my-awesome-campaign",
  "startsAt": 1493355600000,
  "endsAt": 1496206800000,
  "description": "My awesome weekend campaign.",
  "avatar": {
    "src": "https://asdf.cloudfront.net/asdf.jpg",
    "alt": "",
    "width": 200,
    "height": 200
  },
  "causeId": 17,
  "fundraisingEventId": 39,
  "fundraiserGoalAmount": 10000,
  "originalGoalAmount": 5000,
  "amountRaised": 3402.00,
  "supportingAmountRaised": 8923.00,
  "totalAmountRaised": 12325.00,
  "supportable": true,
  "status": "published",
  "user": {
    "id": 1,
    "username": "UserName",
    "slug": "username",
    "url": "/@username",
    "avatar": {
      "src": "https://asdf.cloudfront.net/asdf.jpg",
      "alt": "",
      "width": 200,
      "height": 200
    }
  },
  "team": {
    "id": 1,
    "username": "Team Name",
    "slug": "teamslug",
    "url": "/+teamslug",
    "avatar": {
      "src": "https://asdf.cloudfront.net/asdf.jpg",
      "alt": "",
      "width": 200,
      "height": 200
    }
  },
  "livestream": {
    "type": "twitch",
    "channel": "tiltify"
  }
}
```

## Fields

|key|description|
|:---|:---|
|**id**<br>integer| This is the id of the event. It is a unique identifier that can be used to always find the event. It will never change.
|**name**<br>string| The name of the campaign.
|**slug**<br>string| The url slug used to route to the campaign. These are unique for each user or team.
|**url**<br>string| An absolute url that will take you to the campaign page.
|**description**<br>md-string| The description of the campaign in markdown format. We support basic markdown functionality, so any common markdown should work.
|**avatar**<br>image| An object representing the image for this campaign. It will fall back when appropriate to the FE / cause avatars if one is not present. It is safe to always render this avatar to represent the campaign.
|**supportable**<br>boolean| Whether or not this campaign is supportable.
|**causeId**<br>integer| A reference to the cause that this campaign supports. All campaigns support a cause.
|**fundraisingEventId**<br>integer| A reference to the fundraising event if the campaign is raising money for a fundraising event. Will be `null` if it is not supporting a fundraising event.
|**originalFundraiserGoal**<br>float| The original goal for the campaign if it has been changed.
|**fundraiserGoalAmount**<br>float| The current goal for the campaign.
|**amountRaised**<br>float| The amount of money raised by this campaign.
|**supportingAmountRaised**<br>float| The amount of money raised by all supporting campaigns. This number is 0.0 for campaigns without supporters.
|**totalAmountRaised**<br>float| The amount of money raised by this campaign and all supporting campaigns for this campaign.
|**startsAt**<br>date| The date of when the campaign starts. (at midnight GMT)
|**endsAt**<br>date| The date of when the campaign ends. (at midnight GMT)
|**livestream**<br>object| An object representing the current livestream for this campaign
|**livestream.type**<br>string| Can be one of the following: twitch,youtube,smashcast,mixer,mlg,image
|**livestream.channel**<br>string| The channel for the livestream
