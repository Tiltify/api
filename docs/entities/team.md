>### Deprecation Notice
>Api V3 is being deprecated on July 1st, 2023. Please consider updating to V5

>[V5 Api Documentation](https://v5api.tiltify.com/api/public)

-----

# Team

A team is user owned and managed group of people.

```js
{
  "id": 387,
  "name": "DerpSquad",
  "slug": "derpsquad",
  "url": "https://tiltify.com/+derpsquad",
  "bio": "",
  "inviteOnly": true,
  "disbanded": false,
  "social": {
    "facebook": "tradechatonyoutube",
    "twitch": "tradechat",
    "twitter": "tradechat",
    "website": "",
    "youtube": "tradechat"
  },
  "avatar": {
    "src": "https://asdf.cloudfront.net/asdf.jpg",
    "alt": "",
    "width": 200,
    "height": 200
  }
}
```

## Fields

|key|description|
|:---|:---|
|**id**<br>integer| This is the id of the team.
|**name**<br>string| The name of the team.
|**slug**<br>string| The url slug used to route to the team. These are unique for each team
|**url**<br>string| An absolute url that will take you to the team page.
|**bio**<br>string| A biography for the team
|**inviteOnly**<br>boolean| Whether or not the team is invite only
|**disbanded**<br>boolean| Whether or not the team has been disbanded
|**social**<br>object| A key value object with a team's social id's
|**avatar**<br>image| An image object for the team's avatar
