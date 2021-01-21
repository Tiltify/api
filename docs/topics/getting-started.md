# Getting Started

This will walk you through the steps to get started with using our API.

## 1. Create a Tiltify account.

You need a Tiltify account to access our API. Creating one is free, and only
takes a few moments.

[Sign Up](https://tiltify.com/users/sign_up)

## 2. Create an OAuth Application.

To create an Oauth application, start by [going to your dashboard](https://dashboard.tiltify.com/), clicking on the grid menu icon, clicking "My account", going to the "Connected accounts" tab, and then clicking "Your applications" on the side. If you don't plan on using OAuth2, just use
`https://example.com` as the redirect URI.

## 3. Begin Making Requests.

We provide Applciation Access Tokens for ease of use. Just start by making
requests, and adding your access_token to the Authorization header.

```
Authorization: Bearer <access_token>
```
