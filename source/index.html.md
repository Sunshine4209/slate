---
title: API Reference

language_tabs:
  - php

toc_footers:
    - <a href='http://localhost:4567/rpc.html'>Rpc Documentation</a>
    - <a href='http://localhost:4567'>Rest Documentation</a>
  
includes:
  - errors
  - changeLog

search: true
---

# Rest API

Au cours de la guerre de Sécession, cinq Nordistes : l'ingénieur Cyrus Smith et son chien Top, le reporter Gédéon Spilett, le Noir Nab, le marin Pencroff et le jeune Harbert, prisonniers des troupes séparatistes, se sont enfuis en balIon. Pris dans la tempête, ils échouent sur une île déserte, en plein océan Pacifique.
Ingénieux, persévérants, les cinq compagnons, pourtant privés de tout, ne tardent pas à s'organiser, à vivre presque normalement. D'ailleurs, l'île, qu'ils baptisent du nom de Lincoln, offre des ressources admirables et tout à fait inattendues. Mais une série de faits inexplicables, des coïncidences troublantes les obligent à croire à la présence d'une puissance mystérieuse qui les épie sans cesse et conduit leur destinée, leur imposant sa volonté par des voies détournées, intervenant pour les sauver aux moments critiques

## API Standard Response

> sample response without errors

```json
{
        "success": true,
        "code": [],
        "data": [],
        "total_rows": 0,
        "returned_rows": 0,
        "private_key": null,
        "public_key": null
}
```

Name | Description
---- | ------------
success | true or false whether the call succeeded or not
code | an array of error response codes, each response code is described per call.
data | an array of a single model returned by the call. 
total_rows | The total number or rows you have access to.
returned_rows | The total number or rows returned.
next | The url for the next set of objects. It will be null if there are no more objects to retrieve. `Only for GET calls`.
prev |  The url for the previous set of objects. It will be null on the first page or if there are no more objects to retrieve. `Only for GET calls`.
private_key | Private key used to encode urls. It will be sent only when authenticating with Basic Auth.
public_key | Public key is returned along with a private key on call authenticated with Basic Auth. Use this key to authenticate subsequent calls.


# Member

## The Member Object

Attribute | Type | S | Description
--------- | ---- | --- | ------------
**id** | *uuid*  | T | represent an uuid. Can be set or `auto` generated
first_name | *string* | F | the first name of the user.
last_name | *string* | F | the last name of the user. Lorem ipsum dolor sit amet.
created_on | *datetime* | T | Donec malesuada magna dolor, scelerisque vestibulum ipsum volutpat nec.

<aside class="notice">
S : searchable field, indicate whether the field is searchable.
</aside>


## Get

> The call returns JSON structured like this:

```json
[
    {
        "success": true,
        "code": [],
        "data": [
            {
              "id": "059274be-d4bf-4d5a-b801-de8461d395d4",
              "first_name": "Fluffums",
              "last_name": "calico",
              "created_on": "2016-04-05 00:00:01"
            },
            {
              "id": "d58bcff5-025c-4e4e-93a6-c5af4f2edd22",
              "first_name": "Fluffums",
              "last_name": "calico",
              "created_on": "2016-04-06 00:00:01"
            }
        ],
        "total_rows": 2,
        "returned_rows": 2,
        "private_key": null,
        "public_key": null
    }     
]
```

This endpoint retrieves all kittens.

### HTTP Request

`GET http://alpha.busy.com/member?_version=3.2`

### Query Parameters

Parameter |  Description
--------- | -----------
id | If set the result will only return that particular member.
first_name | If set to false, the result will include kittens that have already been adopted.

### Error Codes

Error Code | Meaning
---------- | -------
400 | Bad Request -- Your request sucks
401 | Unauthorized -- Your API key is wrong
403 | Forbidden -- The kitten requested is hidden for administrators only



<iframe style="width:500px; height: 500px; background-color: #ffffff;" frameborder="0" src="http://localhost:4567/disqus.html"> </iframe>

[try it now](http://busybusyvero.getsandbox.com/hello) you can also [Discuss it](https://busybusy.slack.com/)

## Post

> The call returns JSON structured like this:

```json
[
    {
        "success": true,
        "code": [],
        "data": [
            {
              "id": "059274be-d4bf-4d5a-b801-de8461d395d4",
              "first_name": "Fluffums",
              "last_name": "calico",
              "created_on": "2016-04-05 00:00:01"
            }
        ],
        "total_rows": 1,
        "returned_rows": 1,
        "private_key": null,
        "public_key": null
    }     
]
```

This endpoint retrieves all kittens.

### HTTP Request

`POST http://alpha.busy.com/member?_version=3.2`

### Query Parameters

Parameter | Required | Description
--------- | -------- | -----------
id | false | If set the result will only return that particular member.
first_name | true | If set to false, the result will include kittens that have already been adopted.
last_name | true | If set to false, the result will include kittens that have already been adopted.
created_on | false | default to `1970-01-01 00:00:00`.

# Organization

            
