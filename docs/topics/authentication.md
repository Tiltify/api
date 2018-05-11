# Authentication

Our Api uses OAuth2 to authenticate to endpoints.

Access is delegated to access tokens upon authentication, and the access_token
as of the v3 API will not have an expiry time.

This may change in a future api version.

## Oauth

OAuth2 Authorize URL

```
https://tiltify.com/oauth/authorize
```

OAuth2 Token URL

```
https://tiltify.com/oauth/token
```

## Using Access Tokens

Simply add the Authorization header to your HTTP request.

```
Authorization: Bearer <access_token>
```

Example:

```
Authorization: Bearer 10b56ef89e09702d4dda5860d9e5c37db0af44bcb7cb49d869be94438ad58294
```

#### Application Access Tokens

For ease of use, we have provided an Application Access Token. This grants you
access to the API without having to have users OAuth into your application.


#### Cause Endpoints
Some cause endpoints require additional authorization to use but will return forbidden if the access level is not granted by the used token.
