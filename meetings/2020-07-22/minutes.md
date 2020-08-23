# Me eting Minutes - RSocket TSC

**Location**: Virtual Zoom

**Date**: July 22, 2020

**Time**: 3pm GMT

## Attendance

**Board**: 
 
 * Oleh Dokuka
 * James Townley
 * Steve Gury
 * Stephane Maldini
 * Simon Baslé
 * Jackie Chen
 * Yuri Schimke
 * Rossen Stoyanchev
 * Spencer Gibb
 
 
## Agenda Items

1. Status Report: 
    * RSocket-Java: 
        * Ongoing refactoring on the infrastructure/internals.
        * New interface - `RSocketClient`. `RSocket` is the interface, but now we have `RSocketClient` and accept `Mono`/`Flux` as input. That makes `ByteBuf` pooling easier, and works like a `WebClient`/`HttpClient` and replaces `Mono<RSocket>` with `RSocketClient`. Shared state.
        * ***TODO***: Needs to verify if other language bindings can use this approach.
    * RSocket-Cpp:
        * Project is not actively maintained
        * Facebook created a new [C++ implementation which is coupled with Thrift](https://github.com/facebook/fbthrift/tree/master/thrift/lib/cpp2/transport/rocket).
        * Alibaba will be contributing and providing `CompositeMetadata` implementation
        * ***TODO***: Need to check whether it is possible to use existing RSocket-Cpp in the new RSocket-Thrift so the last one will be just a higher level of abstraction
    * RSocket-JS:
        * Project is not actively maintained 
        * Facebook uses this project only by one team. 
        * ***TODO***: Ping Steve Gury, so he connect with representative from this team in order to avoid any breaking changes for them in the further project maintenence
    * RSocket-Python/RSocket-Go/RSocket-Rust/RSocket-Ruby/RSocket-Dart
        * Maintained by Alibaba
        * Needs review to see what is missing at this point
    * RSocket-Swift
        * Missing at this point
        * Alibaba will be looking for developer to bootstrap the project
    * RSocket-TCK
        * Resurected from scratch 
        * ***TODO***: Call for volunteers 
1. Docs & Guides
    * ***TODO***: take a look at ReactiveX webpage for inspiration
    * Rossen volunteered to work out basic docs
    * Reactive Foundation is hiring a technical writer to help with docs
1. RSocket Spec
    * Leasing:
        * Lease Setup phase remains unchanged
        * ***TODO***: Introduce lease strategies so the client offers what strategies it supports and then server accepts that and sends back with the first lease accepted strategy used for the whole interaction. Or reject if none of the provided strategies are acceptable

