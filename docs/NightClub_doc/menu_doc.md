---
layout: default
title: Menus
parent: Night Club
nav_order: 2
---
## Menus

List of all routes:
* [List all menus](#List-All-Menus)
* [Get active menu](#Active-Menu)
* [Update menu](#Update-Menu)
* [Set Menu to Active](#Set-Active-Menu)
* [Create new menu](#Create-new-Menu)
* [Delete menu](#Delete-Menu)

___

### List All Menus

* **GET https://nite-apigateway.herokuapp.com/nightClub/menus/** - List all menus from one night club

Requires token in header (*Bearer token*) from employee or manager.


___

### Active Menu

* **GET https://nite-apigateway.herokuapp.com/nightClub/menus/active** - Retrieve active menu from one night club

    * FOR CONSUMER:
        Requires token in header (*Bearer token*) from consumer.
        Sends info in query.params (*idNightClub*): `/menu/active?idNightClub=YYYY`
    
    * FOR EMPLOYEE/MANAGER
        Requires token in header (*Bearer token*) from employee or manager.
        Info of night club is already in token!

___

### Update Menu

* **PUT https://nite-apigateway.herokuapp.com/nightClub/menus/{id}** - Update a menu

Requires token from manager.

```js
req.body = {
    menu_name: String,
    menu_status: Boolean,
    menu_description: String,
    menu_products: Array[{
        product_name: String,
        product_category: String,
        product_price: Number,
        product_id: String
    }]
}
```

___

### Set Active Menu
* **PUT https://nite-apigateway.herokuapp.com/nightClub/menus/active** - Set menu to active

Requires token from manager.

```js
req.body = {
    id : String
}
````

___

### Create new Menu
* **POST https://nite-apigateway.herokuapp.com/nightClub/menus/** - Create new menu

Requires token from manager.

```js
req.body = {
    menu_name: String,
    menu_status: Boolean,
    menu_description: String,
    menu_products: Array[{
        product_name: String,
        product_category: String,
        product_price: Number,
        product_id: String
    }]
}
```

___

### Delete-Menu
* **DELETE https://nite-apigateway.herokuapp.com/nightClub/menus/{id}** - Deletes menu

Requires token from manager


