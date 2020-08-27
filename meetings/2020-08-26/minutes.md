# Me eting Minutes - RSocket TSC

**Location**: Virtual Zoom

**Date**: August 26, 2020

**Time**: 3pm GMT

## Attendance

**Board**: 

 * Ryland Degnan
 * Rossen Stoyanchev
 * Seteve Gury
 * Spencer Gibb
 * Oleg Yukhnevich
 * Jacky Chen
 * Oleh Dokuka

 
 
**Notable Guests***
 
## Agenda Items

* Call to Order
* Agenda is Approved
* RSocket Implementations Status Updated
    * RSocket-Java:
        * 1.1.0-M1 release
        * New Loadbalancer API
        * New RSocketClient API
    * RSocket-Kotlin:
        * New Pure-Kotlin Implementation based on the Ktor and Kotlin 1.4
    * RSocket-Rust:
        * Alibaba is actively working on the RUST impl (more focus on integrity with Deno)
        * there is some rewriting related to webassembly support
    * RSocket-Ruby
        * there is no feedback from ruby devs ( *TODO* possible spreads more news for ruby devs )
        * no support for the RxRuby framework (there is a fork from the origin RxRuby but there is no activity).
        * *TODO* look whether Reactive Foundation can take over RxRuby to help with the development
    * RSocket-Python
        * *TODO* need code review
        * CompositeMetadata and Routing Metadata extensions in the PRs
    * RSocket-Net
        * Signed Nuget Package (certificate is on Oleh's name for now)
    * RSocket-Cpp
        * maintain mode
    * RSocket-JS
        * no updates 

* Docs & New: 
    * no progress on docs
    * Blog at rsocket.io
        * Articles related to RSocket
        * Real Stories from big companies
        * Recent news and updates 
        * new features updates with explanation
        * Interviews
    
* RSocket-Spec:
    * Leasing Changes: 
        * what if the server does not understand any of lease strategies
            * fallback to the default one (weaker impl)
            * another - strict one
        * *TODO* clarify compatibility cases old client connects to the new Server as well as the new client connects to the old server or any server which does not support 
        * server has to always respond with the selected strategy encoded in the metadata to have the same behavior 
        * if the leasing strategy is not specified then the new client has to fallback to the default (request count strategy) one (which implicitly means that server is from the old generation)
        * if the client does not support the default strategy (request count), then the client may close the connection and re-establish it again without leasing enabled
        * consider new type - `handshake frame` in order to agree on leasing strategy (Action Point for Ryland)