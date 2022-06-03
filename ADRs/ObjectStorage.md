# Object Storage: Spotlight will use object storage

## Status

APPROVED

## Context

The Spotlight App requires handling readable content such as PDFs. This content must have good availability and the storage needs to be scalable to handle multiple file requests simultaneously.


## Decision

* We will use a public cloud hosted object store to store pdf files.


## Consequences

#### Positive
* Object store can handle pdf files. 
* It will store any associated metadata if needed.
* We wont have to deal with availability, SLA metrics, and infrastructure needs for object store since it will be in public cloud.

#### Negative
* Costs can be high if capacity is not kept in check.


#### Risks
* Data consistency: Files could become corrupt based on the underlying storage technique/hardware.
