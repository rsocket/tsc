# Meeting Minutes - RSocket TSC

**Location**: Virtual Zoom

**Date**: July 05th, 2022

**Time**: 3pm GMT

## Attendance

**Board**:

Oleh Dokuka
Spencer Gibb
Niclas Kristek
Gabi Shaar
Oleg Yukhnevich
Rossen Stoyanchev
Kevin Viglucci

**Notable Guests**:

Roman Mullier

## Agenda Items

- Welcome word for Gabi (main contributor to RSocket-py) and Roman (representative from illumy - contributing to RSocket-Swift).
- News
- RSocket at LFX Crowdfunding (<https://crowdfunding.lfx.linuxfoundation.org/projects/bb4066fb-8137-4557-8224-f17dba073494>)
  - We need to do a proper budget split to make contribution more appealing (item for : Oleh and Rossen)
- Implementations updates:
  - RSocket-Java:
    - There are a couple of issues from the Spring side which has to be resolved. (<https://github.com/spring-projects/spring-framework/issues/27462>, <https://github.com/spring-projects/spring-framework/issues/27427>)
  - RSocket-Kotlin:
    - QUIC integration
    - Resume 2.0 integration
  - RSocket-JS:
    - fixing bugs in new RSocket-JS 1.0.x
    - GraphQL implementation over Apollo in progress
  - RSocket-Swift:
    - Need to check what we need to change to support QUIC. (<https://github.com/netty/netty-incubator-codec-quic>)
    - CompositMetadata for Auth support is ongoing
- GraphQL over RSocket
  - Talk to Apollo Federation to blog abour GraphQL over RSocket (Rossen going to bring a connection)
  - Error responses have to be clarified and more strictly specified. We need to finish with error frame. Every individual response can have an error - in that case we need to end the whole stream with an error. Global error can be part of the rsocket error frame
  - RSocket-JS + Apollo has issues with error sending
  - need an extra meeting with Rovssen, Kavin, Oleg and Oleh to ammend the spec wording.
  - Kaving need to find diff between GraphQL-JS and GraphQL-Java imple before the meeting.
  - GraphQL Federation - we need to learn in the spec and see if we can do anything to support RSocket (<https://www.apollographql.com/docs/federation/other-servers>) (<https://github.com/apollographql/federation-jvm>)
