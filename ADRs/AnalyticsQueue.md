# ANALYTICSQUEUE: The Analytics capability will use a queue to store analytics events

## Status
APPROVED

## Context
The analytics capability may generate a large volume of data from candidate actions and other activities. This makes database calls a significant resource constraint if too many events are generated at one time.

## Decision
The analytics capability will use a queue to store analytics data and events.

## Consequences
#### Positive
- Using a queue will allow the analytics API microservice to "buffer" data so that the analytics reporting microservice is not overwhelmed. This will allow the analytics reporting microservice to poll for events and perform database writes as it's resources allow.
- Using a queue increases reliability and prevents analytics data from being lost if the analytics API, analytics reporting service, or analytics database go down or become unresponsible.
- Additional queues could be provisioned to scale with demand if needed.

#### Negative
- Adding an asynchronous queue to the design increases complexity and makes it harder to troubleshoot issues

#### Risks
- If the queue does down or becomes unavailable, analytics data that has not yet been retrieved could become permanantly lost

[Back to ADR List](../ADRs/)