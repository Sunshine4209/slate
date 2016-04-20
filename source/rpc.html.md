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

# RPC API

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


# Account

say something about the params needed, blah blah blah