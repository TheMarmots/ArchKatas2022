# LoginTypes: Spotlight will support one login mechanism at the start

## Status

APPROVED

## Context

The actors for Spotlight App are primarily non-profits and candidates interested in non-profit services. Login mechanisms under consideration would be simple email address/password combination as credentials and logging in via third-party services using mechanisms like OIDC.

## Decision

* We will support one login mechanism at the start using email addresses and passwords to support ease of use. Logging in using third-party services can be added later.


## Consequences

#### Positive
* Email address and password is a known and simple authentication mechanism.
* The architecture design and software components. 

#### Negative
* Actors will need to have an email address and remember a password.
* Some actors might not want to create a separate account.


#### Risks
* Security: We will have to securely store credentials in a database and if leaked they could pose information exposure risk.
