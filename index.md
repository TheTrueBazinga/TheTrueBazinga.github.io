---
layout: default
title: Home
nav_order: 1
description: "Nite REST API."
permalink: /
---



# Nite App REST API Documentation

# Api-Gateway

## Responde codes

- 200 `OK` - the request was successful.
- 400 `Bad Request` - the request could not be understood or was missing required parameters.
- 401 `Unauthorized` - authentication failed or user doesn't have permissions for requested operation.
- 403 `Forbidden` - access denied.
- 404 `Not Found` - resource was not found.
- 500 `Error` - Error in some process. 

## Routes



### UsersMS
Receive requests from front-end and redirects them to UsersMS
* [Manager DOC](./docs/Users_doc/manager_doc)
* [Employee DOC](./docs/Users_doc/employee_doc)
* [Consumer DOC](./docs/Users_doc/consumer_doc)

____

### NightClubMS

Receive requests from front-end and redirects them to NightClubMS

* [DigitalCards DOC](./docs/NightClub_doc/digitalCards_doc)
* [Menus DOC](./docs/NightClub_doc/menu_doc)
* [Products DOC](./docs/NightClub_doc/products_doc)
* [Categories DOC](./docs/NightClub_doc/categories_doc)
* [Public Relations DOC](./docs/NightClub_doc/rps_doc)

___

### CardsMS

Receive requests from front-end and redirects them to CardsMS. This MS only does operations related to phisical Cards

* [Phisical Cards DOC](./docs/Cards_doc/cards_doc)


