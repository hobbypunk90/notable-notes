---
tags: [Notebooks]
title: distributed tracing
created: '2019-07-30T06:19:49.038Z'
modified: '2019-07-30T07:03:04.213Z'
---

# distributed tracing

`span`  
- individual unit of work, are named and have start+end timestamp

`trace` 
- made of multiple spans
- can be thought of as a `directed acyclic graph`
@startuml
(a)->(b)
(a)->(d)
(b)->(e)
(c)->(d)
(d)->(e)
@enduml

`baggage`
- reference or unique-ID + Data (kev:val) => `span-conect`


[Intro to Distributed Tracing](https://www.kartar.net/2019/07/intro-to-distributed-tracing)
[opentracing.io/docs/overview/spans](https://opentracing.io/docs/overview/spans/)


