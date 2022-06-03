# NOTIFYQUEUES: Spotlight will use Event Queues for notifications
## Status

APPROVED

## Context

To support notification scheduling and delivery, Spotlight needs some way to schedule and delivery generic notifications (for various things like training assignment, new offerings, etc.).


## Decision

* We will use event queues to back the majority of the notification capability.


## Consequences

#### Positive
* Using an event queue for notification scheduling helps guarantee that notifications are delivered even if certain services are temporarily down.
* It also guarentees that notifications aren't delivered multiple times by different mechanisms. e.g. if you view "notifications" in the UI before the email trigger happens, the event will be queued and you won't get a duplicate email notification.

#### Negative
* Additional complexity: This is one of the few places event queues are used which adds additional implementation effort.


#### Risks
* High queue backlogs may cause performance issues or unexpected UX. May need to consider when to "abort" events.
