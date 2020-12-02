# Meeting Minutes - RSocket TSC

**Location**: Virtual Zoom

**Date**: December 2, 2020

**Time**: 3pm GMT

## Attendance

**Board**: 
Rossen Stoyanchev
Simon Baslé
Oleh Dokuka
Oleg Yukhnevich
 
**Notable Guests***
 
## Agenda Items

* Call to Order ✅
* Approval of the Agenda ✅
* RSocket State Report: ✅
    * Implementations Report 
        * *TODO* Prepare a feedback form. Collect opinion from know users of RSocket 
        * RSocket-JS
            * Ask Jacky Chan for support and review
            * Ask Steve Gury for review (just general overview from someone from FB side who is aware of JS state)
            * Call for joining the initial RSocket-JS call  
            * *TODO For Oleh*: invite everyone from the RSocket community to join the call
            * *TODO* ask Intuit folks for RSocket-JS feedback (possibly ask Trade Republic folks about RSocket-JS)
        * RSocket-Java
            * We have 1.1.0: Better Perf / new Loadbalancing which can be followed in other impl
            * Planning for 1.0.4 and 1.1.1
        * RSocket-Kotlin
            * Currently working is going on 
                * Frame Handling
                * Another approach for backpressure propagation
                * Fragmentation support
                * new version of Kotlin Ktor has better performance
                * Anton Arhipov from dev rel side helping with blogs and news sharing about
                * *TODO For Oleh* talk to Anton about RSocket-Kotlin native app example (Anton and OlgeY collaboration)
        * RSocket-Swift
            * 2 companies decided to help with the impl
            * *TODO for Oleh* share the call link (next week)
* RSocket API:
    * `RequestChannel(Payload, Publisher<Payload>)` vs `RequestChannel(Publisher<Payload>)` ✅
        * `RequestChannel(Payload, Publisher<Payload>)` in those implementations where a reactive library does not support `switchOnFirst` operator
        * *TODO* add somewhere info about the reasons to go with the first API or the second
    * Extention API (negotiation, phase for negotiation, etc) (postponed to the next meeting) ➡️
* RSocket Spec:
    * ErrorPayload updates
        * The idea is to add 
        * *TODO for Rossen* to look at https://github.com/rsocket/rsocket/issues/282
    * Ressumability 2.0: Should we use it for Streams only (postponed to the next meeting)=
    * GraphQL
        * Building a protocol similar to RSocket
        * *TODO* Talk to FB folks to see if we can collaborate
        * https://github.com/enisdenjo/graphql-ws
        * https://github.com/enisdenjo/graphql-ws/blob/master/PROTOCOL.md
        * *TODO for Rossen* to take a look at https://github.com/rsocket/rsocket-rpc-java/tree/master/rsocket-ipc-graphql/src/main/java/io/rsocket/graphql