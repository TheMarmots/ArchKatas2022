# Authentication Capability

## Diagram

![AuthCapability](https://raw.githubusercontent.com/TheMarmots/ArchKatas2022/main/assets/AuthCapability.svg)

## Description

The Auth capability is broadly responsible for handling user auth (handling login/logout, password reset, etc) as well as internal service support (RBAC).

## Use Cases

* Registration
* Login
* Internal Service RBAC
* Session Token Generation
## Components

* Auth DB: Used for storing user info, session token metadata, and roles.
* Auth Capability Microservice: Primary logic used by routes and other microservices.
* Session Token: Signed token (e.g. JWT, but does not have to be) that represents a signed user session. Does NOT include role info.

## Architectural Characteristics
* Security
* Availability
* Performance

## ADR
- [RBACinAUTH](../../ADRs/RBACinAUTH.md)
- [LoginTypes](../../ADRs/LoginTypes.md)
- [AuthDB](../../ADRs/AuthDB.md)

[Back to Capabilities List](../../Solution/DetailedArch.md)