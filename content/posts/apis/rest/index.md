+++
title = 'ReST APIs -- and hypermedia as the engine of application state  '
date = 2023-10-21T20:58:54+02:00
draft = true
+++

## Intro


## Idea
ReST is an abstraction, a architecture style pattern based on HTTP and the core web principles. It uses things like HTTP or hypermedia, like html, in the way it was orginally invented for the web. 

One of the core principle is the strong server side logic: Besides the HTTP web api, where a client have to decide what has to be done next, the server offers oppurtonities to a client to choose from. This leads to an dynamic interaction, which is based on hypermedia affordness, like links, dynamic forms, link relations, etc. Therefore it supports a discovery journey during the runtime instead of static dev-time-hard-coded if-elses. 

Using this approach means using a highly evolvable approach: Instead of versioning in some URIs we add some additional resources. 


## To come from HTTP to ReST
Remember our table? Let's use it and make it restful! Instead of define this in this statically way...: 

| URI                                        | METHOD | MEANING                                                |
|--------------------------------------------|--------|--------------------------------------------------------|
| https://store.com/v1/customers             | POST   | create a new customer                                  |
| https://store.com/v1/customers/{id}        | GET    | get customer details                                   |
| https://store.com/v1/customers/{id}/orders | GET    | get a list of customer's details (here his/her orders) ||

... create a service document to dynamize it. A service document is a machine readable document, written e.g. in XML or JSON. For our example above it would be something like: 

```json
{
  "serverDescription": {
    "base":  "https://store.com/",
    "links": [
      {"rel": "all", "href": "/orders/"},
      {"rel": "all", "href": "/orders/"},
      {"rel": "received", "href": "/orders/received/"},
      {"rel": "accepted", "href": "/orders/accepted/"},
      {"rel": "rejected", "href": "/orders/rejected/"},
      {"rel": "cancelled", "href": "/orders/cancelled/"},
      {"rel": "fulfilled", "href": "/orders/fulfilled/"},
      {"rel": "cancelations", "href": "/cancelations/"},
      {"rel": "reports", "href": "/reports/"}
    ] 
  }
}
```
Advantage: Server sends this to a client. A client can use the links, voilá: a dynamic interaction!

Tools like [json-home](https://apievangelist.com/2017/08/03/api-discovery-using-json-home/) supports us to put this into a api definition. 

[//]: # (TODO: Wirklich?)

If we want more dynamics, we can create resource links. That means, we don't define a static document, like the example json above for navigation. Instead we return a list of links from the server to the client within the respsonse. Advantage: We can easily add further extension to this list. 

And if you want even more Rest, we can create a state machine on server side and send the status transition between the states to the client.




[//]: # (#### BILD)

[//]: # (#### BILD)

###  Bingo points ReST
- loosest coupling
- dynamic
- evolve things without destroy others
- generic semantic
- use for longterm needs

### Nays
- harder to use
- server can not decide it independently, clients have to able to use this
