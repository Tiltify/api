# Causes

A cause is something.

```json
{
  "id": 35,
  "name": "St. Jude Children's Research Hospital",
  "slug": "stjude",
  "url": "https://stjude.tiltify.com",
  "about": "* St. Jude Children's Research Hospital is leading the way the\nworld understands, treats and defeats childhood cancer and other\nlife-threatening diseases.  \n* Your support helps ensure that families never receive a bill\nfrom St. Jude for treatment, travel, housing or food -- because all a family\nshould worry about is helping their child live.  \n* St. Jude has helped push the childhood cancer survival rate\nfrom less than 20% when we opened to 80% today. We won't stop until no child\ndies from cancer.",
  "contactEmail": "playlive@stjude.com",
  "video": "https://asdfasdfasdf.cloudfront.net/1234.jpg",
  "image": "https://asdfasdfasdf.cloudfront.net/1234.jpg",
  "avatar": "https://asdfasdfasdf.cloudfront.net/1234.jpg",
  "logo": "https://asdfasdfasdf.cloudfront.net/1234.jpg",
  "bannerSrc": "https://asdfasdfasdf.cloudfront.net/1234.jpg",
  "bannerAlt": "some text describing the banner",
  "currency": "USD",
  "bannerTitle": "St. Jude Children's Research Hospital",
  "bannerIntro": "Start a fundraising campaign to help us end childhood cancer.",
  "social": {
    "twitter": "stjude",
    "youtube": "stjude",
    "facebook": "stjude",
    "instagram": "stjude",
    "snapchat": "stjude",
  },
  "legal": {
    "name": "ST JUDE CHILDRENS RESEARCH HOSPITAL INC",
    "copyright": "© Copyright 2017. St. Jude Children's Research Hospital, a not-for-profit, section 501 (c)(3) corporation.",
    "coppa": "https://example.com/coppa",
    "privacy": "https://example.com/privacy-policy",
    "terms": "https://example.com/terms-and-conditions"
  },
  "address": {
    "address_line_1": "262 DANNY THOMAS PL MSC 512",
    "address_line_2": "",
    "city": "MEMPHIS",
    "region": "TN",
    "postal_code": "38105-3678",
    "country": "US"
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
