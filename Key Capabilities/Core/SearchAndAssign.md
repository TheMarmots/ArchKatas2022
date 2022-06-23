# Search and Assign Capability

## Diagram
![AssignmentCapability](https://raw.githubusercontent.com/TheMarmots/ArchKatas2022/main/assets/SearchAssignCapability.svg)

## Description
The Search and Assign capability is reponsible for searching and assigning the registered community leaders and career mentors to non-profits and candidates, respectively. The data on community leaders and career mentors as well as primary candidate and non-profit information required to match are stored in a persistent storage, shared between the two services. The shared data store helpes in optimizing the database queries, thereby optimizing the searches.

## Use Cases
* Search matches for community leader as per the non-profit type, tags, location and availability
* Search matches for career mentor as per the candidate interests, tags, location and availability
* Automatically select the most relevant matches that are closest to the non-profit and candidate needs
* Assign community leader to a new non-profit during intake workflow
* Assign career mentor to a new candidate during intake workflow

## Components
* Search and match service: search implmentation to query backend by applying specific parameters
* Assignment service: use the matches and assign them to the new non-profit and candidate
* Data persistent storage


## Architectural Characteristics
* Availability
* Scalability
* Performance
* Search Accuracy


## ADR
- [SearchQuery](../../ADRs/SearchQuery.md)
- [DBCertain](../../ADRs/DBCertain.md)
- [AssignStrategy](../../ADRs/AssignStrategy.md)

[Back to Capabilities List](../../Solution/DetailedArch.md)