# DBREADREPLICATION: Spotlight will make use of DB Read Replication

## Status

APPROVED

## Context

One of the most common actions in the system will be reading previously stored persistent data. This will be need to be accomplished very quickly otherwise reads will become a bottleneck to the overall system.


## Decision

* The persistence capability will use DB read replicas


## Consequences

#### Positive
* Read replicas will drastically speed up read time and enable scalability long-term.

#### Negative
* Replication delay could cause slightly outdated data to be returned. Note: we don't consider this a huge problem since our system uses events to write data as well, so there's never a guarentee you're reading current data.


#### Risks
* Slightly outdated data could be returned at any time and clients and use-cases must recognize this.

[Back to ADR List](../ADRs/)