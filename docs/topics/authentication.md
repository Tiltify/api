>### Deprecation Notice
>Api V3 is being deprecated on July 1st, 2023. Please consider updating to V5

>[V5 Api Documentation](https://v5api.tiltify.com/api/public)

-----

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

## Getting A User Access Token

The method to get a user access token generally follows OAuth2. The following is a specific example of how to retrieve A User Access token using OAuth2

### Getting the code

This example will be using the following values as needed.
Application ID: 1234
Redirect https://www.example.com/redirect
Secret Key: asdf

To begin with, send a user in a browser to the Tiltify OAuth Authorization url. Include your Client ID, and the response type of `code` as query parameters.
You may include your redirect URI if you have more than one, as well as a state parameter. A space separated list of scopes may also be added, however, if not included, the `public` scope will be automatically selected.

```
https://tiltify.com/oauth/authorize?&client_id=1234&response_type=code&redirect_uri=https%3A%2F%2Fwww.example.com%2Fredirect&state=54321&scope=public
```

After signing in and authorizing, the user will be redirected back to your chosen redirect URI with a query parameter of `code`, containing the code used to fetch the access token, as well as a `state` parameter should one have been included when the user was sent to the authorization URL.

```
https://www.example.com/redirect?code=1234abcdef&state=54321
```

The code should be passed to your server backend as the following steps require your secret key, which should not be exposed to the public.

### Converting The Code To A User Access Token

To retrieve the User Access Token, a post request must be made to the Token URL. In the body of the url are the following fields in Form Data format. Note specifically that code is the code retrieved from the first step.

```
client_id=1234
redirect_uri=https://www.example.com/redirect
code=1234abcdef
grant_type=authorization_code
```

An Authorization header must also be included following the Basic Auth standard, having a value of `Basic <base64-encoded(Application ID:Secret Key)>`. In this example case, this is `Basic MTIzNDphc2Rm`

Tiltify will return a json object like the following

```
{
   "access_token": "<the user access token>",
   "token_type": "Bearer",
   "scope": "public",
   "created_at": 12345667890
}
```

This access token may now be used as shown below to make requests. When used with the [/user](/endpoints/user.md) endpoint, the full [Users](/entities/user.md) object is returned.

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
