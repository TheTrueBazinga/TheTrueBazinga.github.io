---
layout: default
title: Establishment's DB
parent: Establishment's DB
nav_order: 2
---

## Establishments Managment

List of all routes:
* [Add Establishment](#add-establishment)
* [List all Establishments](#list-all-establishments)

___

### Add Establishment

* **POST https://nite-apigateway.herokuapp.com/nightClub/nightClubDatabase** - Add one establishment to Database

```js
req.body = {
    nightClub_id: String,
    nightClub_name: String,
    nightClub_url: String,
    nightClub_secret: String
}
```


### List all Establishments
* **GET https://nite-apigateway.herokuapp.com/nightClub/nightClubDatabase** - List all establishment's names

