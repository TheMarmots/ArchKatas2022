# FORUMSTORAGE: The Forum capability will use the persistent storage capability as it's database

## Status
APPROVED

## Context
The forum capability needs to store potentially a lot of data. The data will likely be persisted for a long time, and need to be highly available.

## Decision
The forum capabiltiy will use the persistent storage capability as the data store for forum operations.

## Consequences
#### Positive
- The persistent storage capability emphasizes eventual consistency and high availability, which are two characteristics needed by the forum
- No additional infrastructure is needed, reducing complexity

#### Negative
- Coupling to the persistent storage capability could present challenges with maintenance and updates to the forum microservice

#### Risks
- If the persistent storage capability becomes unavailable or loses data, the forums will not be able to operate
