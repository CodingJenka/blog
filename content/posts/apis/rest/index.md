+++
title = 'ReST APIs -- and hypermedia as the engine of application state  '
date = 2023-11-09T20:58:54+02:00
draft = false
+++

## Intro
After we know HTTP is a [application protocol](https://codingJenka.github.io/blog/posts/apis/http) we can dive into ReST, short for _Represential State Transfer_. 

## Idea
First of all: ReST is nothing physical. It doesn't exist as '_anything_'. It's an abstraction of the web. It uses its core principles and behaviour to create a universal communication architecture.

## ReSTs standalone feature
Since HTTP as a web protocol implements many of these principles, it is a convenient tool for creating a ReST API
However, HTTP alone does not make an API ReSTful. 

A ReSTful API is characterized by hypermedia driven communication, i.e. the server responses contains links thus represent an offer to the client for suitable next actions. And since the execution of an action transfers the client to a new state, the server opens up further states for the client in this manner, starting from its current state.

This main characteristic of ReST is called **_HATEOAS_**, short for _hypermedia as the engine of application state_. 

This type of communication, i.e. the server tells the client which states it can reach next, simultaneously means a strong server-side logic. This leads, first, to a decoupling of the client from the actual business logic.

Furthermore, it is a type of runtime discovery journey: Instead of using hard-coded if-else statements on the client side to transit into a new state because of the servers response, we shift this kind exploration into the runtime and rely entirely on the server response. This leads, secondly, to the maximum possible decoupling between client and server. and that in turn means: Every type of client is able to communicate with the server.

Additional plus: ReST is very versatile. Instead of versionize in some URIs ("/v1/"), you can add some additional resources with an updated version to the links within your response.


## Fundamental principles of ReST
After this rough overview, let's take a closer look at the basic principles of ReST: 

1. _**Resources can be identified by a unique identifier (URI)**_
A URI always describes exactly one resource. However, on resource can be described by different URIs.  <br> <br>
2. **_Resources have different representations (XML, JSON, HTML...)_**
As I said before, a resource is not a physical thing. It's an abstraction. To make it visible, we need a kind of representation for it. A resource may have different representations, e.g. a resource can be returned both as HTML page and as a JSON (depending on what representation it has and/or what the client explicitly requested). The ressource is always the same, but represented in different ways.  <br> <br>
3. **_There is a set of standard methods which can be applied to any resource._** HTTP supports us with its buckets (GET, POST, PUT, DELETE...) we talked before. This fixed set of operations allows a client to request resources from the server. Due to the standardization, the server is able to understand this correctly.  
 Secondly, a fixed set of methods defines also guarantees for the client: It knows exactly what type of responses it can be expected. This also defines what kind of responses is a valid response. <br> <br>
4. **_The communication is stateless_**
That means, there is no history or memory. Everytime a client called the server, it's like a brand-new client. <br> <br>
5. **_The communication is link and hypermedia driven_**
Tada: THE magic ingredients for making an API ReSTful. Instead of defining a static URI like https://store.com/v1/customers the client requested the server and receive a server representation back, like: 
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

[//]: # (Here we see possible next states for the client. )

[//]: # (If some states are not reachable from the current one the server will not transmit this as an opportunity to the client &#40;e.g. cancellation of an order is from a certain state on not possible anymore&#41;. )


## To come from HTTP to ReST
Remember our table from the [HTTP post](https://codingJenka.github.io/blog/posts/apis/http)? Let's use this and make it ReSTful!!!!! 

Instead of define this in this statically way...: 

| URI                                        | METHOD | MEANING                                                |
|--------------------------------------------|--------|--------------------------------------------------------|
| https://store.com/v1/customers             | POST   | create a new customer                                  |
| https://store.com/v1/customers/{id}        | GET    | get customer details                                   |
| https://store.com/v1/customers/{id}/orders | GET    | get a list of customer's details (here his/her orders) ||

... create a service document to dynamize it. A service document is a machine readable document, written e.g. in XML or JSON. For our example above it would be something like we saw some lines before: 

```json
      {"rel": "all", "href": "/orders/"},
      {"rel": "all", "href": "/orders/"},
      {"rel": "received", "href": "/orders/received/"},
      {"rel": "accepted", "href": "/orders/accepted/"},
      {"rel": "rejected", "href": "/orders/rejected/"},
      {"rel": "cancelled", "href": "/orders/cancelled/"},
      {"rel": "fulfilled", "href": "/orders/fulfilled/"},
      {"rel": "cancellations", "href": "/cancellations/"},
      {"rel": "reports", "href": "/reports/"}
```
A Server sends this static document to a client. A client can choose the right links and voilá: A dynamic interaction!

Tools like [json-home](https://apievangelist.com/2017/08/03/api-discovery-using-json-home/) supports us to put this into a API definition. 

If we want to add more dynamics, we can go further and create _resource links_. This means, we don't define a static document. Instead, we return a list of links from the server to the client within the response. Advantage: We can easily add further extension to this list. 

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
Next step would be to create a state machine on the server and represent the status transition between those states to the client. The client can follow this and adopt a new state. 


---
### Comparison
After we discus the main characteristics (hypermedia) of ReST and saw how we can turn a HTTP API into a ReSTful one, let's assume some pros and cons: 

| Bingo points ReST                            | Nays                                                                     |
|----------------------------------------------|--------------------------------------------------------------------------|
| Loosest coupling                             | Harder to initial implement                                              |
| Dynamic exploration via the runtime          | Server can not decide it independently, clients have to able to use this |
| Evolve things without destroy others         |                                                                          |
| Generic semantic                             |                                                                          |
| Standard exchange formats, like XML, JSON... |                                                                          |
| Use for longterm needs                       |                                                                          |


