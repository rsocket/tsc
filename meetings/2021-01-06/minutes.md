# Meeting Minutes - RSocket TSC

**Location**: Virtual Zoom

**Date**: January 6th, 2021

**Time**: 3pm GMT

## Attendance

**Board**: 

 - Oleg Yukhnevich
 - Niclas Kristek
 - Oleh Dokuka
 - Rossen Stoyanchev
 - Simon Basle
 
**Notable Guests***
 
## Agenda Items

Call to Order ✅
* Approval of the Agenda ✅
* Implementations reports
    - RSocket-Kotlin ✅
        - Reassembly work is ongoing
        - Kotlin Scripting Support
    - RSocket-Swift ✅
        - Havily in development
        - Frame Parsing is ongoing
        - Swift-NIO as base
        - multilibrary approach (core (frames, reactive-streams types) | )
    - RSocket-JS ✅
        - had a call with Rossen, Oleh, Biran Clozel
* RSocket API:
    * Extention API (negotiation, phase for negotiation, etc) TODO
        - what usecase for EXT do we need it at all?
        - negotiation phase? (http://www.noiseprotocol.org/)
        - should stream-id be 0? 
        - Extension should be used to add new Frames into communication (who can send?) - both sides
        - do we need to understand which extensions are enabled at the moment
        
