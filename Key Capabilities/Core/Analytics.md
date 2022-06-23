# Analytics Capability

## Diagram
![AnalyticsCapability](../../assets/Analytics%20Capability.svg)

## Description
The analytics capability allows the Spotlight service to aggregate data about how candidates use the service and where they are most engaged, see matches and signups for offerings, and help administrators understand where there might be gaps for in-demand offerings.

## Use Cases
- Operational reports for administrators which show things like signups and engagement for non profit offerings and offerings per region
- Analytical reports for administrators which show things like candidate engagement on certain topics and offering gaps in certain regions 

## Components
- Analytics API Microservice
- Event Queue
- Analytics Reporting Microservice
- Analytics Reporting Database
- Analytics Frontend

## Architectural Characteristics
- Availability
- Performance
- Scalability

## ADR
- [AnalyticsDB](../../ADRs/AnalyticsDB.md)
- [AnalyticsQueue](../../ADRs/AnalyticsQueue.md)
- [AnalyticsAPI](../../ADRs/AnalyticsAPI.md)
