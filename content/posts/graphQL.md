+++
title = 'graphQL'
#date = 2023-10-21T20:58:54+02:00
draft = true
+++

## Intro


## Idea
Is a language for interaction with graph based data models, tunneled via HTTP-Post. Allows to query and change (mutate) data. 

Allows an recursive selection of desired nodes and properties. 

As a client i am able to tell exactly what i expect. 
There are some standards for navigation through a huge result sets via pagination. It offers a subscription functionality for recognize changes. 
Also a lot of tools are available for different functionalities for the client as well as for the server side. As a client, there are tools for caching or offline availability (local caching after pulling from a server, update notification). Serverside tools mostly for enabling the usage of other things, like bridging to existing APIs or databases. 

Native query syntax, JSON output. 

## Buckets...again
As with HTTP, the concept of semantic buckets is a good approach to establishing re-usability in graphQL. Hence we find three concepts: 
- query
- mutation 
- subscription. 

Query contains things like ```get_X()```, ```find_Y()``` or ```list_Z()```. ```initiate()```, ```submit()```, ```update()``` or ```cancel()``` belongs to the mutattion bucket und subscription is something like ```getNewInfos()```.  

[//]: # (Similar to HTTP, it's a standardized semantic, but now with an qery.)

### When to use it... 
... imho only when you accesing your graph based data in _unforeseen_ way and your server is almost a kind of a data store                                                     


### Nays...
- Leads to a amount of client side logic, if ypu still have server side business logic (and your server isn't only a data storage), graphQL is not your friend
- You will have a tight coupling between your client and your data <br/> <br/> _Let me explain this:_ <br/> The naturally functionality of a client is containing one sort of logic: the presentation logic. With graphQL your queries encapsulated a lot of business logic, too. This adds another kind of logic to the client: Business logic. The client tended to be a rich one. These, now, two functionalities of your client doesn't stick that much together like teh business logic and the base data. Hence the client is much tighter coupled to the data than it's second functionality, the presentation logic. <br/> R.I.P SoC :(
- Adding tools over tools to server for using _something_ blow up your server complexity 
- Sending high complex queries to your server and your server needs much more resources to solve this than planned? ouch... there is a risk to kill your server with your client


[//]: # (#### BILD)

[//]: # (#### BILD)


