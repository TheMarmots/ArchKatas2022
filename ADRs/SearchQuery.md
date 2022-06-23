# SEARCHQUERY: Spotlight will support faster and accurate searches

## Status

APPROVED

## Context

The search capability is primarily used in intake functionality. As it is required to automatically find matching leaders and mentors, inline with the intake workflow, speed and accuracy are key.  

## Decision

* Support for searching closest matches by using various search parameters such as tags, availability, location preferences etc.
* Support memcache of search results for speed and performance

## Consequences

#### Positive
* Reduces the manual selections and inputs during intake process, making it seamless
* Improves speed of search for the inline intake process

#### Negative
* Additional cache maintenance and refresh needed
* Query parameters can be too specific

#### Risks
* Cache refresh can hinder accuracy, can return stale results
  
[Back to ADR List](../ADRs/)