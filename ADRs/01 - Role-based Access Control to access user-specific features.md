# 01- Role-based Access Control to access user-specific features

## Status

DRAFT

## Context

The Spotlight App is used by three major types of users who have access to different functionality within the app. 

From security and usability perspective, it is important that the users perform actions according to their role. Controlling access based on role prevents privilege escalations, protecting the data integrity. 


## Decision

* Assign user roles at the time of registration
* Apply role restriction on functionalities and services within the app and its backend


## Consequences

#### Positive
* Layer of security through authorization.
* Systematic way to distinguish between types of users and track the usage.

#### Negative
* Requires additional checks on proper role restrictions on services
* Adding new roles will require backend changes

#### Risks
* If implemented poorly (e.g. spoofable request parameters), this can allow users to escalate their privileges vertically.

