# Causes

A cause is something.

```js
{
  "id": 35,
  "name": "St. Jude Children's Research Hospital",
  "slug": "stjude",
  "url": "https://stjude.tiltify.com",
  "currency": "USD",
  "about": "* St. Jude Children's Research Hospital is leading the way the\nworld understands, treats and defeats childhood cancer and other\nlife-threatening diseases.  \n* Your support helps ensure that families never receive a bill\nfrom St. Jude for treatment, travel, housing or food -- because all a family\nshould worry about is helping their child live.  \n* St. Jude has helped push the childhood cancer survival rate\nfrom less than 20% when we opened to 80% today. We won't stop until no child\ndies from cancer.",
  "video": {
    "src": "https://www.youtube.com/watch?v=dQw4w9WgXcQ",
    "alt": "synthesize distributed solutions",
    "width": 640,
    "height": 360
  },
  "image": {
    "src": "https://asdf.cloudfront.net/asdf.jpg",
    "alt": "synthesize distributed solutions",
    "width": 640,
    "height": 360
  },
  "avatar": {
    "src": "https://asdf.cloudfront.net/asdf.jpg",
    "alt": "synthesize distributed solutions",
    "width": 64,
    "height": 64
  },
  "logo": {
    "src": "https://asdf.cloudfront.net/asdf.jpg",
    "alt": "synthesize distributed solutions",
    "width": 64,
    "height": 100
  },
  "banner": {
    "src": "https://asdf.cloudfront.net/asdf.jpg",
    "alt": "synthesize distributed solutions",
    "width": 530,
    "height": 1440
  },
  "bannerTitle": "St. Jude Children's Research Hospital",
  "bannerIntro": "Start a fundraising campaign to help us end childhood cancer."
}
```

## Fields

|key|description|
|:---|:---|
|**id**<br>integer| This is the id of the cause. It is a unique identifier that can be used to always find the cause. It will never change.
|**name**<br>string| The name of the cause.
|**slug**<br>string| The url slug used to route to the cause. These are unique for each cause
|**url**<br>string| An absolute url that will take you to the cause page. This may be on a subdomain.
|**currency**<br>string| The currency code to describe all amount of money under this cause. This is an ISO 4217 currency code.
|**about**<br>md-string| A short few paragraphs about the cause.
|**video**<br>string| The absolute url of the video used in the "about cause" section.
|**image**<br>string| The absolute url of the image used in the "about cause" section.
|**avatar**<br>string| The absolute url of the thumbnail used to identify the cause. This is square.
|**logo**<br>string| The absolute url of the logo used to identify the cause.
|**bannerSrc**<br>string| The absolute url of the banner used on the cause page.
|**bannerAlt**<br>string| An image description for the banner.
|**bannerTitle**<br>string| The title in the banner of the cause page.
|**bannerIntro**<br>string| The short intro paragraph in the banner of the cause page.
