+++
title = 'gRPC --  '
date = 2023-10-21T20:58:54+02:00
draft = true
+++

## Intro
gRPC based on i an idea i heard on university several times. Each and every time professors discussed this 'like-phyiscal-connection-but-within-distributed-systems' idea i strongly believe, i will never ever have to use this. Old stuff. Nothing comparable like the new fancy tools and approaches. But never say never: Google took on this topic in 2015, puts a nice (and maybe bit self loved seeming...) 'g' first and voila: here we are again, groundhog Day!

## Idea
Like i said: The base idea to divide tasks over different nodes in a distributed network without having the feeling that these tasks are being processed by distributed systems. In the best case, tasks are processed as delay-free as possible, just as if they were carried out by a single machine. 
RPC is fundamentally a local procedure that was scaled to the distributed world using gRPC. 

## Technical basic
gRPC is technically a client/server-communication-pattern. 

[//]: # (#### BILD)

In order for both of them to be able to communicate with one another in a meaningful and goal-oriented manner, two ingredients are first required: 
* a common language 
* a kind of communication adapters on each side


### A common language 
> The limits of my language mean the limits of my world.
> -- <cite>Ludwig Wittgensteins</cite>
 




## Why it makes sense to skale up to the distributed world
