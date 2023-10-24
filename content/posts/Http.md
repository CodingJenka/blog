+++
title = 'HTTP -- this thing what you think it is ReST  '
date = 2023-10-21T20:58:54+02:00
draft = true
+++

## Intro


## Idea
Http, Hypertext transfer protocol, is a stateless application protocol. Application, because it's a protocol of the application layer of the ISO/OSI layer model of the web (= layer 7), which is used by application for exchanging information. The unit of a exchange information between client and server is a message, which is built of a header with some metadata on the first side and secondly of the actual message body. Messages from a client to a server is called request. A answer from the server back to the client is a response. 
Stateless is similar to memory- or history-less: Every session is brand new one. 

Http delivers some semantic features which can be used for a client/server communication. The most important feature are the so called HTTP verbs. Famous ones are GET, POST, PUT and DELETE. These are like buckets for some basics operations. That means: Using a GET implies reading something, it's for consuming activities. POST is used for creating something new. This will be accessible via an URI afterwards. PUT is a plane update and DELETE is... ja... you know...
Besides POST all of the others from this list are idempotent. 

Almost each and every one of your API methods can be sorted in one of these four buckets (and if not: There are a couple more verbs). Having these semantic buckets means having some generic usable tools for the communication between different applications. Having generic usable tools means having a lot of other tools which can be used to deal with it, e.g.: 

- the browser knows what to do for debugging, 
- browser caches exists because the know the behaviour and communication pattern as well as message format between different applications
- we can use tools like curl for calling something 
- we are language agnostic, that means we can create a HTTP api with every programming language ans use a suited library for translate out methods into HTTP-speech


## Technical basic
The most common way to define a HTTP web api is to describe it like the following example shows. 

| URI                                        | METHOD | MEANING                                                |
|--------------------------------------------|--------|--------------------------------------------------------|
| https://store.com/v1/customers             | POST   | create a new customer                                  |
| https://store.com/v1/customers/{id}        | GET    | get customer details                                   |
| https://store.com/v1/customers/{id}/orders | GET    | get a list of customer's details (here his/her orders) ||


[//]: # (#### BILD)

[//]: # (#### BILD)

###  Bingo points HTTP web apis
- uses the HTTP semantic 
- URI focused
- string focus on server side logic
- standar exchange formats, like XML, JSON...
- API description support by tools, like OpenAPI/Swagger


###  Pros and cons
| Yay                    | nay                                                                                             |
|------------------------|-------------------------------------------------------------------------------------------------|
| Easy to use            | static usage of a dynamic approach                                                              |
|                        | -> also means creating a static relationship between client and server                          |
| Generic semantic       | URIs a re part of the API description (that means: the position of your params become important |
| Wide tool support      | Changes of URI means changing of your API                                                       |
| Widely accepted        | Tighter coupling                                                                                |
| Low demand on consumer | Limited compatibility                                                                           |
|                        |                                                                                                 |

### Attention
`Against the common usage, BUT:
Avoid to use this kind of API style for public APIs you have to maintain over a while.`

It's your contract to the outer world. If you make.e.g. the structure of a URI part of your API description, you sent some hard facts to the outer world. Your clients will relay on this information. Changing the URI, maybe because of some versioning, means breaking the contract. 
