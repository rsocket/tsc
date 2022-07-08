# Meeting Minutes - RSocket TSC

**Location**: Virtual Zoom

**Date**: June 24th, 2021

**Time**: 3pm GMT

## Attendance

**Board**: 

David,
Rossen,
Oleh,
Kevin,
Simon,
Niclas,
 
**Notable Guests***
 
## Agenda Items


1. Conferences
    - Spring One:
        * Wide audience;
        * RSocket Keynote;
        * Various of other talks: RSocket-Kotlin, RSocket at Canva, RSocket intro, rsocket with event sourcing
        * website improvements - testemonials section;
        * (TODO: Rossen) chat with springone marketing folks to check about banner
        * (TODO) add videos to the website
    - Reactive Summit:
        * ping Phil from Blizzard about kenote proposal (he is interested but not available for the time of the conference)

2. Implementation updates
    - rsocket-kotlin:
    - rsocket-swift:
        * Decode / Encode pipes are suported (CompositeMetadata, Routing and other extensions are suported)
        * Impl for all other extensions are in progress
        * Support for native structured concurrency from the latests swift-beta
        * almost production ready
    - rsocket-js: 
        * licensing pre-approval
        * rsocket-typescript effort (should be 1.0 once the impl is done)
    - rsocket-dotnet:
        * Kevin will be playing around with that impl making sure it works in unity

3. RSocket-RPC:
    - rsocket-java-rpc
    - rsocket-js-rpc
    - we dont have a dedicated maintainers
    - other impl are not present

