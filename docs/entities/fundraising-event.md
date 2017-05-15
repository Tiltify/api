# Fundraising Event

A fundraising event is an event organized by a cause with schedules and
incentives.

```js
{
  "id": 1,
  "name": "Big Event 2017",
  "slug": "big-event-2017",
  "url": "https://tiltify.com/cause-slug/big-event-2017",
  "description": "Play For More Than Bragging Rights\r\n\r\nSign up to create your own campaign and start fundraising. Play and stream your favorite video games to raise donations and unlock exclusive loot.\r\n\r\nSt. Jude has helped push the childhood cancer survival rate from less than 20% when we opened to 80% today. We won’t stop until no child dies from cancer.",
  "video": "https://www.youtube.com/watch?v=e-ORhEE9VVg",
  "image": "https://asdfasdfasdf.cloudfront.net/1234.jpg",
  "logo": "https://asdfasdfasdf.cloudfront.net/1234.jpg",
  "avatar": "https://asdfasdfasdf.cloudfront.net/1234.jpg",
  "bannerSrc": "https://asdfasdfasdf.cloudfront.net/1234.jpg",
  "bannerAlt": "Some text describing the banner image",
  "bannerTitle": "St. Jude PLAY LIVE",
  "bannerIntro": "Play video games and create a fundraising campaign to help kids battling cancer.",
  "currency": "USD",
  "goal": 10000,
  "amountRaised": 8923,
  "startsOn": "2017-03-24",
  "endsOn": "2017-03-26"
  "causeId": 17,
}
```

## Fields

|key|description|
|:---|:---|
|**id**<br>integer| This is the id of the fundraising event. It is a unique identifier that can be used to always find the event. It will never change.
|**name**<br>string| The name of the fundraising event.
|**slug**<br>string| The url slug used to route to the fundraising event. These are unique for each cause
|**url**<br>string| An absolute url that will take you to the fundraiisng event page.
|**description**<br>md-string| The description of the fundraising event in markdown format.
|**video**<br>string| The absolute url of a video the fundraising event uses in its about section.
|**image**<br>string| The absolute url of an image or video fallback the fundraising event uses in its about section.
|**logo**<br>string| The absolute url of an image used as the logo for the fundraising event.
|**avatar**<br>string| The absolute url of an image used as the avatar for this fundraising event.
|**currency**<br>string| The currency code to describe all amount of money under this campaign. This is an ISO 4217 currency code.
|**goal**<br>float| The current goal for the fundraising event.
|**amountRaised**<br>float| The amount of money raised by this fundraising event.
|**startsOn**<br>date| The date of when the campaign starts. An ISO 8601 formatted date.
|**endsOn**<br>date| The date of when the campaign ends. An ISO 8601 formatted date.
|**causeId**<br>integer| A reference to the cause that this fundraising event is for.
