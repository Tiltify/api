>### Deprecation Notice
>Api V3 is being deprecated on July 1st, 2023. Please consider updating to V5

>[V5 Api Documentation](https://v5api.tiltify.com/api/public)

-----

# Causes

A cause is something.

```js
{
  "id": 35,
  "name": "Good Cause",
  "legalName": "Good Cause Inc",
  "slug": "goodcause",
  "currency": "USD",
  "about": "We do good stuff",
  "video": "https://www.youtube.com/watch?v=dQw4w9WgXcQ",
  "image": {
    "src": "https://asdf.cloudfront.net/asdf.jpg",
    "alt": "",
    "width": 640,
    "height": 360
  },
  "avatar": {
    "src": "https://asdf.cloudfront.net/asdf.jpg",
    "alt": "",
    "width": 64,
    "height": 64
  },
  "logo": {
    "src": "https://asdf.cloudfront.net/asdf.jpg",
    "alt": "",
    "width": 100,
    "height": 64
  },
  "banner": {
    "src": "https://asdf.cloudfront.net/asdf.jpg",
    "alt": "",
    "width": 530,
    "height": 1440
  },
  "contactEmail": "asdf@example.org",
  "paypalEmail": "asdf@example.org",
  "paypalCurrencyCode": "USD",
  "social": {
    "twitter": "stjude",
    "youtube": "",
    "facebook": "stjude",
    "instagram": "stjude"
  },
  "settings": {
    "colors": {
      "background": "#fff",
      "highlight": "#ce2f40"
    },
    "headerIntro": "Start a fundraising campaign to help us do good things.",
    "headerTitle": "Good Cause",
    "footerCopyright": "© Copyright 2017. Good Cause Inc",
    "findOutMoreLink": "https://www.example.com/find-out-more"
  },
  "status": "published",
  "stripeConnected": true,
  "mailchimpConnected": false,
  "address": {
    "addressLine1": "123 Some St",
    "addressLine2": "",
    "city": "Houston",
    "region": "TX",
    "postalCode": "77008",
    "country": "US"
  }
}
```

## Fields

|key|description|
|:---|:---|
|**id**<br>integer| This is the id of the cause. It is a unique identifier that can be used to always find the cause. It will never change.
|**name**<br>string| The name of the cause.
|**slug**<br>string| The url slug used to route to the cause. These are unique for each cause
|**currency**<br>string| The currency code to describe all amount of money under this cause. This is an ISO 4217 currency code.
|**about**<br>md-string| A short few paragraphs about the cause.
|**video**<br>string| The absolute url of the video used in the "about cause" section.
|**image**<br>image| An image object for the image used in the "about cause" section. It may be null.
|**avatar**<br>image| An image object of the avatar used to identify the cause. This is square.
|**logo**<br>image| An image object of the logo used to identify the cause. May be null
|**banner**<br>image| An image object of the banner used at the top of the cause page.
