# Campaigns

A campaign is the event you create to fundraise for your favorite cause.

```json
{
  "id": 1,
  "name": "My Awesome Campaign",
  "slug": "my-awesome-campaign",
  "url": "https://tiltify.com/@username/my-awesome-campaign",
  "description": "My awesome weekend campaign.\n Save the kids.",
  "thumbnail": "https://asdfasdfasdf.cloudfront.net/1234.jpg",
  "causeId": 17,
  "userId": 14,
  "teamId": null,
  "fundraisingEventId": 39,
  "currency": "USD",
  "goal": 10000,
  "originalGoal": 5000,
  "amountRaised": 8923,
  "totalAmountRaised": 12325,
  "startsOn": "2017-03-24",
  "endsOn": "2017-03-26"
}
```

## Fields

|key|description|
|:---|:---|
|**id**<br>integer| This is the id of the event. It is a unique identifier that can be used to always find the event. It will never change.
|**name**<br>string| The name of the campaign.
|**slug**<br>string| The url slug used to route to the campaign. These are unique for each user or team.
|**url**<br>string| An absolute url that will take you to the campaign page.
|**description**<br>md-string| The description of the campaign in markdown format. We suport basic markdown functionality, so any common markdown should work.
|**thumbnail**<br>string| The absolute url of the thumbnail used to identify the campaign
|**causeId**<br>integer| A reference to the cause that this campaign supports. All campaigns support a cause.
|**userId**<br>integer| A reference to the user who created this campaign.
|**teamId**<br>integer| A reference to the team if the campaign is a team campaign. Will be `null` if the campaign is not a team campaign.
|**fundraisingEventId**<br>integer| A reference to the fundraising event if the campaign is raising money for a fundraising event. Will be `null` if it is not supporting a fundraising event.
|**currency**<br>string| The currency code to describe all amount of money under this campaign. This is an ISO 4217 currency code.
|**goal**<br>float| The current goal for the event.
|**originalGoal**<br>float| The original goal for the event if it has been changed.
|**amountRaised**<br>float| The amount of money raised by this campaign.
|**totalAmountRaised**<br>float| The amount of money raised by this campaign and all supporting campaigns for this campaign. If there are no supporting campaigns, this number is the same as the amountRaised.
|**startsOn**<br>date| The date of when the campaign starts. An ISO 8601 formatted date.
|**endsOn**<br>date| The date of when the campaign ends. An ISO 8601 formatted date.
