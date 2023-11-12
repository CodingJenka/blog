+++
title = 'graphQL'
date = 2023-11-14T20:58:54+02:00
draft = true
+++

## Intro.
GraphQL, a product once launched by Facebook, promises the simple creation of a web architecture. The client is at the center of this query and mutation language. It can specifically request the data it needs. Parameterization promises traffic that is limited to the essentials. 

The question arises: _If the client knows exactly what it currently needs, doesn't it perhaps know a little too much?_

## Idea.
GraphQl is a _language_ (!!) for interactions with graph based data models, tunneled via HTTP-Post. It allows to query and change (mutate) data as well as subscribe to changes for realtime updates. 

Contrary to popular belief, GraphQl can actually only be used for a very limited number of applications. Namely, when we are dealing with tree-like data structures that need to be queried differently in different contexts. 

Implementing tree searching algorithm means, of cause: A recursive selection of desired nodes and properties. Such algorithms are efficient, which is of course always an advantage. The other side of the coin, however, is that the syntax and semantics of a specific language must be learned. In addition, you are less agnostic than with ReST, i.e. changes to the graphql api can result in local adaptations. A disadvantage that you almost "never" have when using a standardized protocol, like HTTP for example.

## The Client. And the server. Functionality.
As a client i am able to tell exactly what i expect via graphQL. 
There are some standards for navigation through huge result sets via pagination. It offers a subscription functionality for recognize changes. 
Also a lot of tools are available for different functionalities for the client as well as for the server side. As a client, there are tools for caching or offline availability (local caching after pulling from a server, update notification). Serverside tools mostly for enabling the usage of other things, like bridging to existing APIs or databases. 

If the client determines exactly what it wants to see, then the client must also _know exactly_ what it needs. In my opinion, this is one of the biggest disadvantages of graphQL. The client is taught an unnecessary amount of logic that has to be dealt with. In the worst case, the entire business logic is put into the client. This violates the actual task that the presentation layer should have: Namely the presentation of data. 

Business logic in the client should also ring all the alarm bells: Fat client sends its regards! Not to mention the violation of fundamental principles such as information hiding...

[//]: # (Native query syntax, JSON output. )

## Buckets...again
As with HTTP, the concept of semantic buckets is a good approach to establishing re-usability in graphQL. 

Hence we find three concepts in graphQL: 
- query
- mutation 
- subscription. 

Query contains things like ```get_X()```, ```find_Y()``` or ```list_Z()```. ```initiate()```, ```submit()```, ```update()``` or ```cancel()``` belongs to the mutation bucket und subscription is something like ```getNewInfos()```.  

[//]: # (Similar to HTTP, it's a standardized semantic, but now with an qery.)

### When to use it... 
... imho only when you accessing your graph based data in _unforeseen_ way and your server is almost a kind of a data store.                                                    

## A valid ReST alternative?
The pre-sale argument of graphQL that it is the better ReST is flawed because we are comparing pears with apples here. As we have seen, ReST is universally applicable due to its highly abstract approach. This is questionable with graphQL.

### Nays...
- Leads to a amount of client side logic, if ypu still have server side business logic (and your server isn't only a data storage), graphQL is not your friend
- You will have a tight coupling between your client and your data <br/> <br/> _Let me explain this:_ <br/> The naturally functionality of a client is containing one sort of logic: the presentation logic. With graphQL your queries encapsulated a lot of business logic, too. This adds another kind of logic to the client: Business logic. The client tended to be a rich one. These, now, two functionalities of your client doesn't stick that much together like teh business logic and the base data. Hence the client is much tighter coupled to the data than it's second functionality, the presentation logic. <br/> R.I.P SoC :(
- Adding tools over tools to server for using _something_ blow up your server complexity 
- Sending high complex queries to your server and your server needs much more resources to solve this than planned? ouch... there is a risk to kill your server with your client


[//]: # (#### BILD)

[//]: # (#### BILD)


