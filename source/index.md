---
title: API Reference

language_tabs:
  - HTTP Request

toc_footers:
  - <a href='#'>API End Point for RAC</a>
  - <a href='http://github.com/fahadgudu/slate'>Documentation by Fahad</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the RAC API! You can use our API to access RAC endpoints, which can get information on various projects, systems, and test in our database.


# Authentication
## Sign in
> To authorize, use this URL  :
>  http://52.62.191.47/api/v1/auth/sign_in

`POST http://52.62.191.47/api/v1/auth/sign_in`

```shell
curl "http://52.62.191.47/api/v1/auth/sign_in"
  -H "Content-Type : application/json && Accept : application/vnd.example.v1"
```
> request json

```json

{
    "email": "fahad@gmail.com",
    "password": "password12"
}
```


> The above command returns JSON structured like this:

```json
{
    "data": {
        "id": 4,
        "email": "fahad@gmail.com",
        "name": null,
        "eula_id": null,
        "first_name": "fahad",
        "last_name": "idrees",
        "company": "1",
        "rating": "0.0",
        "status": "active",
        "user_type": "member",
        "provider": "email",
        "uid": "fahad@gmail.com",
        "number_of_ratings": 0,
        "profile_picture": {
            "url": "https://framework-dev.s3.amazonaws.com/profile_pictures/member/profile_picture/4/IMG_0360.JPG"
        },
        "username": "password",
        "device_token": null,
        "device_type": null,
        "uuid_iphone": null,
        "rac_membership_no": null,
        "postcode": null,
        "bio": null,
        "privacy_id": null
    }
}
```

This endpoint Sign in user to AWS server.

## Sign out

> To Logout, use this URL  :
>  http://52.62.191.47/api/v1/auth/sign_out

`DELETE http://52.62.191.47/api/signout`


<aside class="success">
Remember — auth token is always unique for all users!
</aside>

`Headers`

<aside class="notice">
You must add following headers before any API Call
<code>`Content-Type : application/json`</code>
&&
<code>`Content-Type:application/json
    Access-Token:LlI4-55ZaDrP8rCrqpx4hg
    Client:1gi1MZi-phyJP2bkWdnxIA
    Expiry:1455600539
    Uid:fahad@gmail.com
    Token-Type:Bearer`</code>
</aside>


```shell
curl "http://52.62.191.47/api/signout"
  -H "Content-Type:application/json
    Access-Token:LlI4-55ZaDrP8rCrqpx4hg
    Client:1gi1MZi-phyJP2bkWdnxIA
    Expiry:1455600539
    Uid:fahad@gmail.com
    Token-Type:Bearer
"
```
> The above command returns JSON structured like this:

```json
{
    "success": true
}

```
This endpoint Sign out user to AWS server.

## Sign Up

> To Sign Up, use this URL  :
>  http://52.62.191.47/api/v1/auth

`POST http://52.62.191.47/api/v1/auth`


<aside class="success">
Remember — Add header
</aside>

`Headers`

<aside class="notice">
You must add following headers before any API Call
<code>`Content-Type : application/json`</code>
&&
<code>`Content-Type:application/json
    Access-Token:LlI4-55ZaDrP8rCrqpx4hg
    Client:1gi1MZi-phyJP2bkWdnxIA
    Expiry:1455600539
    Uid:fahad@gmail.com
    Token-Type:Bearer`</code>
</aside>

> request json

```json
{
    "first_name": "fahad",
    "last_name": "idrees",
    "full_name": "fahad idrees",
    "email": "fahad1@gmail.com",
    "postcode": 32313,
    "bio": "fsfsdf",
    "suburb": "",
  "password": "password",
  "username": "usernam",
    "profile_picture_url": "https://framework-dev.s3.amazonaws.com/profile_pictures/member/profile_picture/4/IMG_0360.JPG"
}

```



> The above command returns JSON structured like this:

```json
{
    "status": "success",
    "data": {
        "id": 8,
        "email": "fahad1@gmail.com",
        "created_at": "2016-02-02T09:53:34.182Z",
        "updated_at": "2016-02-02T09:53:34.182Z",
        "name": null,
        "eula_id": null,
        "first_name": "fahad",
        "last_name": "idrees",
        "company": null,
        "rating": "0.0",
        "status": "active",
        "user_type": "administrator",
        "provider": "email",
        "uid": "fahad1@gmail.com",
        "number_of_ratings": 0,
        "profile_picture": {
            "url": null
        },
        "username": "usernam",
        "device_token": null,
        "device_type": null,
        "uuid_iphone": null,
        "rac_membership_no": null,
        "postcode": 32313,
        "bio": "fsfsdf",
        "privacy_id": null,
        "suburb": ""
    }
}

```

This endpoint Sign out user to AWS server.

# Members

## Update Member Profile

> To Sign Up, use this URL  :
>  http://52.62.191.47/api/v1/members/4

`PUT http://52.62.191.47/api/v1/members/4`


<aside class="success">
Remember — Add header
</aside>

`Headers`

<aside class="notice">
You must add following headers before any API Call
<code>`Content-Type : application/json`</code>
&&
<code>`Content-Type:application/json
    Access-Token:LlI4-55ZaDrP8rCrqpx4hg
    Client:1gi1MZi-phyJP2bkWdnxIA
    Expiry:1455600539
    Uid:fahad@gmail.com
    Token-Type:Bearer`</code>
</aside>

> request json

```json
{
    "first_name": "fahad",
    "last_name": "idrees",
    "full_name": "fahad idrees",
    "email": "fahad1@gmail.com",
    "postcode": 32313,
    "bio": "fsfsdf",
    "suburb": "",
    "username": "usernam",
    "profile_picture_url": "https://framework-dev.s3.amazonaws.com/profile_pictures/member/profile_picture/4/IMG_0360.JPG"
}

```



> The above command returns JSON structured like this:

```json
{
    "id": 4,
    "first_name": "guudddd",
    "last_name": "idrees",
    "full_name": "guudddd idrees",
    "email": "fahad@gmail.com",
    "eula_id": null,
    "rac_membership_no": null,
    "postcode": null,
    "bio": null,
    "created_at": "2016-01-12T08:49:30.854Z",
    "updated_at": "2016-02-02T10:39:36.777Z",
    "suburb": "Perth",
    "profile_picture_url": "https://framework-dev.s3.amazonaws.com/profile_pictures/member/profile_picture/4/IMG_0360.JPG"
}

```


