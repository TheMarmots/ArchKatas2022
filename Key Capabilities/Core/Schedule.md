# Schedule Capability

## Diagram
![ScheduleCapability](https://raw.githubusercontent.com/TheMarmots/ArchKatas2022/main/assets/ScheduleCapability.svg)

## Description
The scheduling capability is responsible for sending out invites for introductory meetings and recurring meetings. It has a couple of templates locally which it uses for meeting agendas. The scheduling capability microservice uses a third-party collaboration service to send out the meeting invites to users.
This capability and functionality can be deferred. At the start the spotlight app can rely on career mentors and community leaders to send out invites out of band from the system.

## Use Cases
* Scheduling introductory meetings for candidate, career mentor, and non-profits.
* Scheduling recurring meetings for candidate, career mentor, and non-profits.

## Components
* Scheduling capability microservice: This contains primary logic for integrating with a third-party collaboration/scheduling service and also has a couple of meeting templates (one for introductory meeting and another for recurring).
* Third-party collaboration/scheduling service: This service is responsible for actually sending out meeting invites to users' calendars considering the time-zones and time slots.  


## Architectural Characteristics
* Scalability
* Fault-tolerant  

## ADR
- [CollaborationPlatform](../../ADRs/CollaborationPlatform.md)

[Back to Capabilities List](../../Solution/DetailedArch.md)