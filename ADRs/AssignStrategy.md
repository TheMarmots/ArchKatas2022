# ASSIGNSTRATEGY: Spotlight will support automatic assignment of matched leaders and mentors

## Status

APPROVED

## Context

The Search and Assign capability is primarily used in intake functionality. As it is required to automatically assign matching leaders and mentors, inline with the intake workflow, speed and accuracy are key. Additionally, the automatic matching requires some intelligence in the assignment service to choose the right match. 

## Decision

* Support assigning the top match with higest match percentage returned by the search query
* Support saving the assignment information passively as part of data collection, which can be used to build ML models in long-term

## Consequences

#### Positive
* Reduces the manual selections and inputs during intake process, making it seamless

#### Negative
* Additional data capture and storage may be required
* No manual interaction can have a misses initially

#### Risks
* If the assignment of a match is a miss, candidate or non-profit may lose interest due to lack of right support
  
