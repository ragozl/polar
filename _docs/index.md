---
title: Polaris Docs
permalink: /docs/home/
redirect_from: /docs/index.html
---

___

## Types of request classes
Most Polaris API endpoints take one of the two defined class arguments. These arguments should be passed as strings, even if you are giving a number. We do this purely for convenience, as it's easier to remember to just ```tostring``` or ```str()``` something for example.

Here are the two types of requests we accept:
### RequestUser
```json
{
  "owner_secret": "your_owner_secret",
  "gameid": "123456",
  "userid": "123456"
}
```

### RequestNoUser
```json
{
  "owner_secret": "your_owner_secret",
  "gameid": "123456"
}
```

We will tell you which endpoints use which, so please refer back to this or keep it in your mind while you read the documentation.

___

## Request types
The following endpoints use the following methods:

- /auth/create_mod : POST
- /auth/check : POST 
- /auth/remove_mod : POST
- /auth/mods : POST

___

## Authentication
In this section, we will be showing you authentication endpoints. These have functionality like checking if a ID is a moderator, adding moderators, etc.

### /auth/create_mod
`Request Type: Request User`
This endpoint will create a moderator for your game. Please note that you **really need to practice good security** checks on the server administering requests for this. Use this with the combination of the **/auth/creds** endpoint to make sure that the user performing the action is whitelisted (only supports Roblox/Discord ID's, if you would like more, post a suggestion)

### /auth/check_mod
`Request Type: Request User`

