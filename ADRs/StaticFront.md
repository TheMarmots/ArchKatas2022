# ROUTEHANDLERS: STATICFRONT

## Status

APPROVED

## Context

The Spotlight App uses will have a considerable amount of user-facing web UI along with many different backend API flows. We need to decide on some way to manage these two portions of the overall architecture.


## Decision

* The frontend will exist as a fully static, client-side web app that can be bundled and deployed independently of the API services


## Consequences

#### Positive
* Full separation makes iteration on the UI much easier. This is critical since usability is one of our primary goals. We do not want frontend and UX teams to have to understand the instrictincies of server-side rendering to improve the experience of the frontend.

#### Negative
* UI could be slower if we need to load a large amount of data from the server.


#### Risks
* While we don't anticipate the frontend needing to display a huge amount of data, there is some risk a use-case will come up that requires it. This could cause significant UI performance issues.
