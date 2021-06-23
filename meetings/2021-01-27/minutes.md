# Meeting Minutes - RSocket TSC

**Location**: Virtual Zoom

**Date**: January 27th, 2021

**Time**: 3pm GMT

## Attendance

**Board**: 

Stephane Maldini
Oleh Dokuka
Oleg Y
Rossen Stoyanchev
Niclas Kristek
Simon Basle
Spancer Gibb

 
**Notable Guests***
 
## Agenda Items

Call to Order
* Approval of the Agenda
* News
    * new look for rsocket.io
    * more interest to rsocket protocol
* Implementations reports
    * RSocket-JS
        * 2 maintenence releases
        * most of issues are closed 
    * RSocket-Java
        * new router api which (based on composite metadata route extension)
    * RSocket-Kotlin
        * fragmentation is coming
        * KotlinX serialization support is coming
    * RSocket-Swift
        * RSocket Responder part is in progress
* RSocket API:
    * 1.0 Approval
        * add hint to metadata `length` in frame header to make it clear how `length` has to be encoded (TODO: Niclas + Oleh D)
        * mark existing lease part as experimental (note that it might be changed to in 2.0)
    * Extention API
        * Create a PR (Simon B) about negotiation phase
    * Resumability 
        
