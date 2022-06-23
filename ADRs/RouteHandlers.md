
# ROUTEHANDLERS: Route Handlers will be implemented via dedicated microservices.

## Status

APPROVED

## Context

The Spotlight App uses a static client <--> Restful HTTP-based API driven architecture for most user-facing functions. This means a series of "routes" must be provided that are well documented and stable.


## Decision

* We will use dedicated Route Handler services to implement route-specific business logic
* Route Handlers may provide more than one route assuming they exist under the same "group" (e.g. a candidate profile route handler may provide list, create, and update routes)


## Consequences

#### Positive
* Clean separation between routes making extensibility easier over time

#### Negative
* Higher cost: We may need to deploy a LOT of services for each route


#### Risks
* None anticipated

[Back to ADR List](../ADRs/)