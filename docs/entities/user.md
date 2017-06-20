# User

A user is a member of the site.

```js
{
  "id": 3,
  "username": "TiltifyUser",
  "slug": "@tiltify-user",
  "url": "https://tiltify.com/@tiltify-user"
  "thumbnail": "https://asdfasdfasdf.cloudfront.net/1234.jpg",
  "status": "completed"
}
```

## Fields

|key|description|
|:---|:---|
|**id**<br>integer| This is the id of the user.
|**username**<br>string| The username of the user.
|**slug**<br>string| The url slug used to route to the user. These are unique for each user.
|**url**<br>string| An absolute url that will take you to the user page.
|**thumbnail**<br>image| A users avatar
|**status**<br>string| A Users registration status
