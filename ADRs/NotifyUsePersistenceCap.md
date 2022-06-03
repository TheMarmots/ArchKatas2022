# NOTIFYUSEPERSISTENCECAP: Spotlight will use the persistence capability to store notifications
## Status

APPROVED

## Context

In addition to notification scheduling and delivery, Spotlight needs some way to store notifications that the user has already "seen" (acknowledged) but might still want available. For example, just because you saw that you were "assigned" a course doesn't mean you want the notification gone. Perhaps you want to keep it as a reminder until you're done with the course.


## Decision

* The notification capability will use the persistence capability to store notifications.
* We will explictly NOT use a dedicated database for the notification capability.


## Consequences

#### Positive
* By not using a dedicated database we can help reduce cost and complexity.
* By using the existing Persistence capability we can make use of existing infrastructure.

#### Negative
* Tighter coupling: By not using a totally separate mechanism for storage, debugging will be harder.
* Sensitive to availability of persistence capability: If the persistence capability is unavailable, the notification storage capability will not work as expected.


#### Risks
* Unavailability of the persistence capability will cause strange behavior (missing notification history and state).
