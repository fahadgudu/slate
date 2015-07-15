---
title: API Reference

language_tabs:
  - HTTP Request

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='http://github.com/fahadgudu/slate'>Documentation by Fahad</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the X Operative Tab API! You can use our API to access X Operative Tab endpoints, which can get information on various projects, systems, and test in our database.


# Authentication
## Sign in
> To authorize, use this URL  :
>  localhost:3000/api/signin

`POST localhost:3000/api/signin`

```shell
curl "localhost:3000/api/signin"
  -H "Content-Type : application/json && Accept : application/vnd.example.v1"
```
> The above command returns JSON structured like this:

```json
{
    "email": "hamilton@gmail.com",
    "authentication_token": "nLKSTVuSKmrxUezuWirF",
    "created_at": "2015-07-02T07:50:01.168Z",
    "updated_at": "2015-07-08T05:10:23.770Z",
    "company_id": 6,
    "timestamp": 1436332223.777125
}
```

This endpoint Sign in user to AWS server.

## Sign out

> To Logout, use this URL  :
>  localhost:3000/api/signout?auth_token=wCtXRyxhYk7HTdZpM8eC

`DELETE localhost:3000/api/signout?auth_token=wCtXRyxhYk7HTdZpM8eC`

```shell
curl "localhost:3000/api/signout?auth_token=wCtXRyxhYk7HTdZpM8eC"
  -H "Content-Type : application/json && Accept : application/vnd.example.v1"
```
> The above command returns JSON structured like this:

```json
{
    "email": "fahad@gmail.com",
    "authentication_token": "wCtXRyxhYk7HTdZpM8eC",
    "created_at": "2015-06-11T09:59:13.923Z",
    "updated_at": "2015-07-07T07:48:44.615Z",
    "company_id": 1
}

```
This endpoint Sign out user to AWS server.

# Projects

### HTTP Request

`POST localhost:3000/api/projects.json?auth_token=kDKUhhkg_pkEYQhzXkbH`

## Create Project

```shell
curl "localhost:3000/api/projects.json?auth_token=kDKUhhkg_pkEYQhzXkbH"
  -H "Content-Type : application/json && Accept : application/vnd.example.v1"
```

  > Request Json

```json
{
  "project":{
    "name": "Name is khan",
    "status": "active",
    "location": "Sydney"
  }
}
```

> The above command returns JSON structured like this:

```json
{
    "id": 14,
    "name": "Name is khan",
    "status": "active",
    "location": "Sydney",
    "created_at": 1436255994,
    "updated_at": 1436255994
}

```

### HTTP Request

`POST localhost:3000/api/projects.json?auth_token=kDKUhhkg_pkEYQhzXkbH`

## Update Project

`PUT localhost:3000/api/projects.json?auth_token=kDKUhhkg_pkEYQhzXkbH`

```shell
curl "localhost:3000/api/projects.json?auth_token=kDKUhhkg_pkEYQhzXkbH"
  -H "Content-Type : application/json && Accept : application/vnd.example.v1"
```

  > Request Json

```json
{
  "project":{
    "id": 14,
    "name": "TEST Project",
    "status": "active",
    "location": "Sydney"
  }
}
```

> The above command returns JSON structured like this:

```json
{
    "id": 14,
    "name": "TEST Project",
    "status": "active",
    "location": "Sydney",
    "created_at": 1436255994,
    "updated_at": 1436255994
}

```
## Get All the Projects

```shell
curl "localhost:3000/api/projects.json?auth_token=kDKUhhkg_pkEYQhzXkbH"
  -H "Content-Type : application/json && Accept : application/vnd.example.v1"
```

> The above command returns JSON structured like this:

```json
[
    {
        "id": 10,
        "name": "Name is khan",
        "status": "active",
        "location": "Sydney",
        "updated_at": 1436177134
    },
    {
        "id": 12,
        "name": "Name is khan",
        "status": "active",
        "location": "Sydney",
        "updated_at": 1436177479
    },
    {
        "id": 11,
        "name": "fahad what happen to me",
        "status": "active",
        "location": "lahore",
        "updated_at": 1436177899
    },
    {
        "id": 13,
        "name": "Name is khan",
        "status": "active",
        "location": "Sydney",
        "updated_at": 1436178149
    },
    {
        "id": 14,
        "name": "Name is khan",
        "status": "active",
        "location": "Sydney",
        "updated_at": 1436255994
    }
]
```

### HTTP Request

`GET localhost:3000/api/projects/11.json?auth_token=kDKUhhkg_pkEYQhzXkbH`


### HTTP Request

`GET localhost:3000/api/projects/12.json?auth_token=kDKUhhkg_pkEYQhzXkbH`

## Update Project

`GET localhost:3000/api/projects/12.json?auth_token=kDKUhhkg_pkEYQhzXkbH`

```shell
curl "localhost:3000/api/projects/12.json?auth_token=kDKUhhkg_pkEYQhzXkbH"
  -H "Content-Type : application/json && Accept : application/vnd.example.v1"
```

  > Request Json


> The above command returns JSON structured like this:

```json
{
    "id": 12,
    "name": "Test",
    "status": "active",
    "location": "Sydney",
    "created_at": 1436177479,
    "updated_at": 1436177479
}

```
### HTTP Request

`DELETE localhost:3000/api/projects/12.json?auth_token=kDKUhhkg_pkEYQhzXkbH`

## Delete Project

`DELETE localhost:3000/api/projects/12.json?auth_token=kDKUhhkg_pkEYQhzXkbH`

```shell
curl "localhost:3000/api/projects/12.json?auth_token=kDKUhhkg_pkEYQhzXkbH"
  -H "Content-Type : application/json && Accept : application/vnd.example.v1"
```

  > Request Json


> The above command returns JSON structured like this:

```json
{
    "id": 12,
}

```


# System


## Create System

### HTTP Request

`POST localhost:3000/api/systems.json?auth_token=zSwZQMySVAkk_PncMnp5`


```shell
curl "localhost:3000/api/systems.json?auth_token=zSwZQMySVAkk_PncMnp5"
  -H "Content-Type : application/json && Accept : application/vnd.example.v1"
```

  > Request Json

```json
{
  "system": {
    "name": "Test System",
    "status": "active",
    "project_id": 4
  }
}
```


> The above command returns error if project_id is invalid


```json
{
    "description": "Couldn't find Project with 'id'=344",
    "title": "No Record Found"
}

```

> The above command returns JSON structured like this on success:

```json
{
    "project": {
        "id": 4,
        "name": "test project",
        "status": "active",
        "location": "Sydney",
        "created_at": 1436345732,
        "updated_at": 1436345732,
        "system": {
            "id": 9,
            "name": "Test System",
            "status": "active",
            "created_at": 1436349683,
            "updated_at": 1436349683
        }
    }
}

```

## Update System

### HTTP Request

`PUT localhost:3000/api/systems/3.json?auth_token=zSwZQMySVAkk_PncMnp5`


```shell
curl "localhost:3000/api/systems/3.json?auth_token=zSwZQMySVAkk_PncMnp5"
  -H "Content-Type : application/json && Accept : application/vnd.example.v1"
```

> Request Json

```json
{
  "system": {
    "name": "Test System",
    "status": "active",
    "project_id": 4
  }
}
```


> The above command returns error if project_id is invalid


```json
{
    "description": "Couldn't find Project with 'id'=344",
    "title": "No Record Found"
}

```

> The above command returns JSON structured like this on success:

```json
{
    "project": {
        "id": 3,
        "name": "test project",
        "status": "active",
        "location": "Sydney",
        "created_at": 1436345708,
        "updated_at": 1436345708,
        "system": {
            "id": 4,
            "name": "test the system 1345",
            "status": "deactive",
            "created_at": 1436346669,
            "updated_at": 1436350057
        }
    }
}

```
## Show System

### HTTP Request

`GET localhost:3000/api/systems/3.json?auth_token=zSwZQMySVAkk_PncMnp5`


```shell
curl "localhost:3000/api/systems/3.json?auth_token=zSwZQMySVAkk_PncMnp5"
  -H "Content-Type : application/json && Accept : application/vnd.example.v1"
```


> The above command returns JSON structured like this on success:

```json
{
    "project": {
        "id": 4,
        "name": "test project",
        "status": "active",
        "location": "Sydney",
        "created_at": 1436345732,
        "updated_at": 1436345732,
        "system": {
            "id": 3,
            "name": "test the system for project 4",
            "status": "deactive",
            "created_at": 1436346644,
            "updated_at": 1436348924
        }
    }
}

```

## Delete System

### HTTP Request

`Delete localhost:3000/api/systems/3.json?auth_token=zSwZQMySVAkk_PncMnp5`


```shell
curl "localhost:3000/api/systems/3.json?auth_token=zSwZQMySVAkk_PncMnp5"
  -H "Content-Type : application/json && Accept : application/vnd.example.v1"
```


> The above command returns JSON structured like this on success:

```json
{
    "system_id": 16
}

```

## Show Systems of all projects

### HTTP Request

`GET localhost:3000/api/systems.json?auth_token=zSwZQMySVAkk_PncMnp5`


```shell
curl "localhost:3000/api/systems.json?auth_token=zSwZQMySVAkk_PncMnp5"
  -H "Content-Type : application/json && Accept : application/vnd.example.v1"
```


> The above command returns JSON structured like this on success:

```json
{
    "projects": [
        {
            "id": 3,
            "name": "test project",
            "status": "active",
            "location": "Sydney",
            "created_at": 1436345708,
            "updated_at": 1436345708,
            "systems": [
                {
                    "id": 1,
                    "name": null,
                    "status": null,
                    "created_at": 1436346491,
                    "updated_at": 1436346491
                },
                {
                    "id": 2,
                    "name": "test system",
                    "status": null,
                    "created_at": 1436346491,
                    "updated_at": 1436346491
                },
                {
                    "id": 5,
                    "name": "Name is khan",
                    "status": "active",
                    "created_at": 1436346699,
                    "updated_at": 1436346699
                },
                {
                    "id": 6,
                    "name": "Name is khan",
                    "status": "active",
                    "created_at": 1436346721,
                    "updated_at": 1436346721
                },
                {
                    "id": 7,
                    "name": "Name is khan",
                    "status": "active",
                    "created_at": 1436346887,
                    "updated_at": 1436346887
                },
                {
                    "id": 8,
                    "name": "Name is khan",
                    "status": "active",
                    "created_at": 1436347293,
                    "updated_at": 1436347293
                },
                {
                    "id": 4,
                    "name": "test the system 1345",
                    "status": "deactive",
                    "created_at": 1436346669,
                    "updated_at": 1436350057
                }
            ]
        },
        {
            "id": 4,
            "name": "test project",
            "status": "active",
            "location": "Sydney",
            "created_at": 1436345732,
            "updated_at": 1436345732,
            "systems": [
                {
                    "id": 3,
                    "name": "test the system for project 4",
                    "status": "deactive",
                    "created_at": 1436346644,
                    "updated_at": 1436348924
                },
                {
                    "id": 9,
                    "name": "Test System",
                    "status": "active",
                    "created_at": 1436349683,
                    "updated_at": 1436349683
                }
            ]
        }
    ]
}

```
# Instruments


## Create System

### HTTP Request

`POST localhost:3000/api/instruments.json?auth_token=xq9S8MMzW4FWbGW4XCC4`


```shell
curl "localhost:3000/api/instruments.json?auth_token=xq9S8MMzW4FWbGW4XCC4"
  -H "Content-Type : application/json && Accept : application/vnd.example.v1"
```

  > Request Json

```json

 {
  "instrument": {
    "description": "this is test instruments",
    "manufacturer": "guuduu",
    "serial_number": "12345678",
    "calibration_date": "2011-05-19 10:30:14"
  }
}

```


> The above command returns JSON structured like this on success:

```json

{
    "id": 8,
    "description": "this is test instruments",
    "manufacturer": "guuduu",
    "serial_number": "12345678",
    "calibration_date": "2011-05-19T15:30:14.000Z",
    "created_at": 1436870551,
    "updated_at": 1436870551,
    "company_name": "Allah buksh",
    "user_email": "adman1@gmail.com"
}

```

## Update Instruments

### HTTP Request

`PUT localhost:3000/api/instruments/8.json?auth_token=xq9S8MMzW4FWbGW4XCC4`


```shell
curl "PUT localhost:3000/api/instruments/8.json?auth_token=xq9S8MMzW4FWbGW4XCC4"
  -H "Content-Type : application/json && Accept : application/vnd.example.v1"
```

  > Request Json

```json

 {
  "instrument": {
    "description": "this is test instruments",
    "manufacturer": "guuduu",
    "serial_number": "12345678",
    "calibration_date": "2011-05-19 10:30:14"
  }
}

```


> The above command returns JSON structured like this on success:

```json

{
    "id": 8,
    "description": "this is test instruments",
    "manufacturer": "guuduu",
    "serial_number": "12345678",
    "calibration_date": "2011-05-19T15:30:14.000Z",
    "created_at": 1436870551,
    "updated_at": 1436870551,
    "company_name": "Allah buksh",
    "user_email": "adman1@gmail.com"
}

```

## Delete Instruments

### HTTP Request

`DELETE localhost:3000/api/instruments/8.json?auth_token=xq9S8MMzW4FWbGW4XCC4`


```shell
curl "DELETE localhost:3000/api/instruments/8.json?auth_token=xq9S8MMzW4FWbGW4XCC4"
  -H "Content-Type : application/json && Accept : application/vnd.example.v1"
```


> The above command returns JSON structured like this on success:

```json

{
    "instrument_id": 8
}

```


## GET Instruments

### HTTP Request

`GET localhost:3000/api/instruments.json?auth_token=xq9S8MMzW4FWbGW4XCC4&timestamp=1436869503`


```shell
curl "GET localhost:3000/api/instruments.json?auth_token=xq9S8MMzW4FWbGW4XCC4&timestamp=1436869503"
  -H "Content-Type : application/json && Accept : application/vnd.example.v1"
```

  > Request Json


> The above command returns JSON structured like this on success:

```json

{
    "instruments": [
        {
            "id": 5,
            "description": "this is test instruments 5",
            "manufacturer": "guuduu",
            "serial_number": "12345678",
            "calibration_date": null,
            "created_at": 1436869503,
            "updated_at": 1436869503,
            "company_name": "Allah buksh",
            "user_email": "adman1@gmail.com"
        },
        {
            "id": 6,
            "description": "this is test instruments",
            "manufacturer": "guuduu",
            "serial_number": "12345678",
            "calibration_date": null,
            "created_at": 1436869650,
            "updated_at": 1436869650,
            "company_name": "Allah buksh",
            "user_email": "adman1@gmail.com"
        },
        {
            "id": 7,
            "description": "this is test instruments",
            "manufacturer": "guuduu",
            "serial_number": "12345678",
            "calibration_date": "2011-05-19T15:30:14.000Z",
            "created_at": 1436870522,
            "updated_at": 1436870522,
            "company_name": "Allah buksh",
            "user_email": "adman1@gmail.com"
        },
        {
            "id": 8,
            "description": "this is test instruments updated",
            "manufacturer": "guuduu",
            "serial_number": "1222333333",
            "calibration_date": "2011-05-19T15:30:14.000Z",
            "created_at": 1436870551,
            "updated_at": 1436870657,
            "company_name": "Allah buksh",
            "user_email": "adman1@gmail.com"
        }
    ]
}


```

# Delete Records
## Get all Dleted records

### HTTP Request

`GET localhost:3000/api/get_delete_record?auth_token=zSwZQMySVAkk_PncMnp5&timestamp=143690000`


```shell
curl "GET localhost:3000/api/get_delete_record?auth_token=zSwZQMySVAkk_PncMnp5&timestamp=143690000"
  -H "Content-Type : application/json && Accept : application/vnd.example.v1"
```

> The above command returns JSON structured like this on success:

```json

{
    "Timestamp": 1436946527.126473,
    "delete": [
        {
            "model_name": "Project",
            "model_ids": [
                3,
                5
            ]
        },
        {
            "model_name": "System",
            "model_ids": [
                10,
                11,
                12,
                13
            ]
        }
    ]
}


```



