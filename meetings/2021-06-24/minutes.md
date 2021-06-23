# Meeting Minutes - RSocket TSC

**Location**: Virtual Zoom

**Date**: June 24th, 2021

**Time**: 3pm GMT

## Attendance

**Board**: 

David,
Rossen,
Oleh,
Spencer,
Kevin
 
**Notable Guests***
 
## Agenda Items

* Call to Order
* Approval of the Agenda
* Implementations and board updates
    * rsocket-java: 
        * 1.1.1 - first maintance after 1.1.0 (bugfixes, stabilization)
        * 1.0.5 - final maintance release (small bugfixes in it)
    * rsocket-kotlin
        * it works with rsocket-java and spring messaging
        * preparation for 1.5.0
        * slow maintanece mode
    * rsocket-swift
        * maintanence continued 🎉
        * first version of Payload codecs and full composite metadata support 
        * full TCP transport support
        * Websocket has some gaps but in general ready for use
    * rsocket-js
        * move to TypeScript
        * few contribution from Sergei to move away from FB libs
        * TODO (for Oleh): we need to clarify licence agreement from facebook (reach out to Facebook on that question)
        * possible solution: 
            * replace facebook license (if FB is okay with that)
            * create TS lib from scratch as a fully separate effort
    * rsocket-net
        * what is the state
* Common Routing Mechanism for RSocket
    * Rossen: rsocket-java has a good support by Spring and spring provides greate message handling with declarative handlers route declaration (no need for now to create something for apps). We can create something simple (prefix based)
    * Spencer: prefix based router separation can help for rsocket-broker
    * Rossen: rsocket level routing mechanism should help different application routing mechanism to co-exist
    * https://user-images.githubusercontent.com/5380167/105497677-d6632080-5cc7-11eb-8f4d-444b0c30b333.png
    * Rossen: we can suport multiple things:   
        * one way is artificial rout
        * tag - to communicate to whom it is
        * extra routing composite metadata extension?? (TODO: we need to think about routing CM layout imporovement)
        * https://github.com/rsocket/rsocket-rpc-java/blob/master/rsocket-rpc-core/src/main/java/io/rsocket/rpc/frames/Metadata.java#L20
        * PROPOSAL: wellknow separator at routing spec?
* Common base for RSocket over Protobuf-RPC 
