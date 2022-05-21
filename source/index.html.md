---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

includes:
  - errors

search: true

code_clipboard: true

meta:
  - name: description
    content: Documentation for the NewApp API
---

# Introduction

Welcome to the NewAPP API! You can use our API to access NewAPP API endpoints, which can get information from our database.

We have language bindings in Shell, and JavaScript! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

# Authentication

> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here" \
  -H "Authorization: auth_code"
```

> Make sure to replace `auth_code` with your API key.

NewAPP uses API keys to allow access to the API. You can register a new NewAPP API key at our [developer portal](http://example.com/developers).

NewAPP expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: auth_code`

<aside class="notice">
You must replace <code>auth_code</code> with your personal API key.
</aside>

# SushiTap? NewApp!

## Get All Restaurants

```shell
curl "http://newapp.com/api/restaurants/all" \
  -H "Authorization: auth_code"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 2,
    "owner_id": 2,
    "name": "Max",
    "...": "..."
  },
  {
     "id": 2,
    "owner_id": 2,
    "name": "Max",
    "...": "..."
  }
]
```
This endpoint retrieves all the restaurants.

### HTTP Request

`GET http://newapp.com/api/restaurants/all`

<aside class="alert">
Ditemi voi come fare questo pezzo.
Definite l'endpoint, definite il messaggio, definite l'intera API :)
</aside>

## Get a Specific Restaurant

```shell
curl "http://newapp.com/api/restaurant/1" \
  -H "Authorization: auth_code"
```

> The above command returns JSON structured like this:

```json
{
  "id": 1,
  "owner_id": 1,
  "name": "Max",
  "...": "..."
}
```

This endpoint retrieves a specific restaurant.

### HTTP Request

`GET http://newapp.com/api/restaurant/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the restaurant to retrieve