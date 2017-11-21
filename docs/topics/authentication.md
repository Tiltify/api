# Authentication

Our Api uses Oauth2 to authenticate to endpoints.

Access is delegated to access tokens upon authentication, and the access_token as of the v3 API will not have an expiry time.

This may change in a future api version.

## Cause Endpoints
Some cause endpoints require additional authorization to use but will return forbidden if the access level is not granted by the used token.
