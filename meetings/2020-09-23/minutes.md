# Meeting Minutes - RSocket TSC

**Location**: Virtual Zoom

**Date**: September 23, 2020

**Time**: 3pm GMT

## Attendance

**Board**: 

Ben Christensen
Spencer Gibb
Oleg Yukhnevich
Rossen Stoyanchev
Steve Gury
Oleh Dokuka
 
**Notable Guests***
 
## Agenda Items


* Resumability changes (QUIC and HTTP/3) (https://github.com/rsocket/rsocket/pull/312)
    - was implemented for pretty large system at facebook
    - was not efficient at "that" scale
    - requester specify interest through the R flag and the responder has to confirm sending in first frame R flag set as well
    - add clarafication that position is number of frames sent and not bytes in total (implied position/keepalive/resumeframe definition)   (https://rsocket.io/docs/Protocol.html#implied-position)
    - keep alive does not have to send update for anyevery stream that is resumable
    - Number of Entries - something around 2^21
    - backwards compatibility - 2.0 (no backward compatibility). 
    - we should have an agreement based on the version specified in the spec (some future should be backward compatible but things like resumability and leasing should not)