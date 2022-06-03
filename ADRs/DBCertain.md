# DBCERTAIN: Spotlight will support both guarenteed and non-guarenteed interactions with the persistence store

## Status

APPROVED

## Context

Many capabilities in the overall system will need to store persistent data. For example, the user's profile, the user's preferences, the user's notification history, the user's training history, etc.

Some of these requests *must complete* (like storing a "seen" notifications) while others could fail and just notify the user or client of a failure ("whoops, we couldn't save your profile").


## Decision

* The persistence capability will support interfaces to read/write quickly, aborting if some part of the persistence store is unavailable.
* The persistence capability will support interfaces to guarentee read and writes, even if it takes a long time for the service to become available.
* Event queues will be used to guarentee eventual read/writes/consistency.


## Consequences

#### Positive
* Since the persistence capability is going to be used by a huge number of services, it's critical that it be available. By providing a "guarenteed delivery" abstraction we can help ensure other microservices can benefit from centralized storage.
* Since many actions don't require guarenteed delivery, providing an alternative that behaves more like a "native DB query" will speed up implementaion.

#### Negative
* Additional implementation complexity


#### Risks
* Event queues must be up at all times. Lost messages break the guarentee this service tries to provide.
