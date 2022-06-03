# ANALYTICSAPI: The Analytics capability will use an API service to process incoming events

## Status
APPROVED

## Context
The Spotlight platform may generate a large volume of analytics events, some of which may be done internally by other services. The analytics data itself may be in various formats or require validation.
## Decision
The analytics capability will use a separate microservice to process incoming analytics data and events.

## Consequences
#### Positive
- Using a separate service will allow us to scale that API as needed, depending on the volume of data.
- We can validate the incoming data according to our needs
- We can prevent clients from writing directly to the queue which stores the analytics events.

#### Negative
- adding another service introduces additional complexity into the system, which can make troubleshooting harder
- Adding another service increases maintenance overhead and infrastructure costs

#### Risks
- If the analytics API goes down, we will miss data and events which could impact the accuracy of reporting
