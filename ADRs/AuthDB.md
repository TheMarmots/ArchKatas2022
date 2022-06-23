# AuthDB: Spotlight will use a database for the authentication credential information

## Status

APPROVED

## Context

The Spotlight App requires storage of authentication credentials which are email addresses and passwords. The password information gets securely hashed using a password hashing function before reaching the database via the auth capability microservice.


## Decision

* We will use a database to store email address and passwords. To support redundancy we will use at least two databases which synchronize data between them.


## Consequences

#### Positive
* Persistent storage: A database provides persistent storage for authentication credentials.
* Credentials can be looked up quickly.

#### Negative
* Maintaining a redundant set of databases is costly


#### Risks
* If the databases go down then users will not be able to login or register.
* Data consistency: we have to be careful about authentication data being consistent and read/write times.

[Back to ADR List](../ADRs/)