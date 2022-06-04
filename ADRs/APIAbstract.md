# APIABSTRACT: API Interfaces will be abstracted away from the implementation.

## Status

APPROVED

## Context

The Spotlight App uses a static client <--> Restful HTTP-based API driven architecture for most user-facing functions. This means a series of "routes" must be provided that are well documented and stable.


## Decision

* We will use an infrastructure-based abstraction layer composed of DNS entries and load balancers to separate the API interfaces from the implementation.


## Consequences

#### Positive
* We don't have to deploy API services and directly expose their routes providing an easier (and more extensible) mechanism for adding new functionality.
* Clients won't have to individually handle things like TLS termination, etc. This can be done by the load balancers at this layer.

#### Negative
* Slightly more complexity. Much make sure new routes are added this layer while also connecting the corresponding route handler microservices.


#### Risks
* Increased reliance on the load balancer and proper DNS configuration for availability.
