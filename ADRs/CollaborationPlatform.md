# CollaborationPlatform: Spotlight will integrate with a third-party collaboration and scheduling service

## Status

APPROVED

## Context

Spotlight needs capabilities to schedule meetings between users. 


## Decision

* The scheduling capability with integrate with a third-party collaboration and scheduling platform


## Consequences

#### Positive
* Reduced complexity: Since the third-party service will deal with sending out meeting invites, handling scheduling conflicts (time-slots, time zones, etc.)
* Scalable: we can choose a service which meets our needs and is scalable rather than building the entire functionality from scratch.

#### Negative
* Dependence on third-party service: We will not have complete control.


#### Risks
* If the third-party service goes down then meeting invites/scheduling would be affected.
