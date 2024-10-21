---
title: Welcome
permalink: /docs/home/
redirect_from: /docs/index.html
---

## Types of request classes
Most Polaris API endpoints take one of the two defined class arguments. These arguments should be passed as strings, even if you are giving a number. We do this purely for convenience, as it's easier to remember to just ```tostring``` or ```str()``` something for example.

Here are the two types of requests we accept:
### RequestNoUser
```json
{
  "owner_secret": "your_owner_secret",
  "gameid": "123456"
}
```
### RequestUser
```json
{
  "owner_secret": "your_owner_secret",
  "gameid": "123456",
  "userid": "123456"
}
```
