>### Deprecation Notice
>Api V3 is being deprecated on July 1st, 2023. Please consider updating to V5

>[V5 Api Documentation](https://v5api.tiltify.com/api/public)

-----

# User

A user is a member of the site.

```js
{
  "id": 3,
  "username": "TiltifyUser",
  "slug": "tiltify-user",
  "url": "https://tiltify.com/@tiltify-user"
  "avatar": {
    "src": "https://asdf.cloudfront.net/asdf.jpg",
    "alt": "",
    "width": 200,
    "height": 200
  },
  "about": "I'm the best",
  "totalAmountRaised": 1234.23,
  "social": {
    "facebook": null,
    "twitch": "tiltify",
    "twitter": null,
    "website": null,
    "youtube": null,
  }
}
```

## Fields

|key|description|
|:---|:---|
|**id**<br>integer| This is the id of the user.
|**username**<br>string| The username of the user.
|**slug**<br>string| The url slug used to route to the user. These are unique for each user.
|**url**<br>string| An absolute url that will take you to the user page.
|**avatar**<br>image| A users avatar
|**about**<br>string| A few senetences about user
|**totalAmountRaised**<br>currency| Total amount of money raised by this user (in USD)
|**social**<br>object| Object describing user's social accounts
