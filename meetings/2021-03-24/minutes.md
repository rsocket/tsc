# Meeting Minutes - RSocket TSC

**Location**: Virtual Zoom

**Date**: March 24th, 2021

**Time**: 3pm GMT

## Attendance

**Board**: 

Rossen
Kevin
Niclas
Spencer
Oleg
Oleh
Simon
David
Alan

 
**Notable Guests***
 
## Agenda Items

Call to Order
* Approval of the Agenda
* Implementations reports
    * RSocket Community:
        * need to be reopened https://www.w3.org/community/rsocket/
        * Collect feedback about gRPC usage and see what can be improoved in RSocket to get more people interested in RSocket
        * Performance -> https://github.com/blueperf?type=source
        * find some good gRPC examples and check if RSocket good there
        * Chat with Netflix folks as a big users of gRPC
        * Schedule a call for for performance measurement strategy and build a plan for that (probably Rossen, Alan, Oleh, David, Niclas, Spencer, Kavin)
    * RSocket-Spec:
        * cleanups need review (For Rossen)
    * RSocket-Website:
        * RSocket-Spec at webpage - need sync on protocol text 
        * RSocket-Website preview via Netlifi integration
        * Getting-Started is in progress (For Rossen)
    * RSocket-Swift:
        * Fully based on Swifth NIO (1:1 to Netty Project)
        * Roadmap towards the first release:
            * Websocket transport impl needs review
            * Error handling
            * Combine impl
            * Reconnection (similar to RSocket-Java)
            * Composite Metadata
            * add a PR RSocket-Website to reflect impl presence
            * Wider dependency manageres support
    * RSocket-Kotlin:
        * Fragmentation support is about to PR
        * draft PR for kotlin serialization and RSocket 
    * RSocket-Java:
        * 1.0.4 maintanence release
            * 1.0.x is moving towards EOL
        * 1.1.1 - first mentanence release (planned on April). Includes:
            * Lease refactoring. Main improvements:
                - transperency on the Requester side
                - Simplified API for the responder lease management
                - Examples are based on the deprecated Netflix Concurrency Limitter library (need a chat with someone from Netflix) (for Spencer)
            * Composite Metadata improvements are coming (Per-Stream Data MimeType)
            * Close Error suppport for gracefull shutdown
    * RSocket-JS
        * A few Release 0.0.22 - 23 - 25
        * Buffer Polyfill 
            * 0.1.x - removes out Buffer polyfill 
        * 1.0.x - fully build on TypeScript (for Kavin)
    * RSocket-Dotnet
        * need to sync with Microsoft folks
        * https://github.com/rsocket/rsocket-net/pull/26 need review and feedback
            * Suggest breaking PR on to logical commits to make review easier (for Oleh) 
    * RSocket-Go
        * brings its own impl of Reactive Streams and Reactor (Mono and Flux) (for Alan / Simon / Oleh)
        * we need to have a review (for Alan)
        * Schedule a call for reviewed 
* News
        
