# RBACinAUTH: Spotlight will support role based access control

## Status

APPROVED

## Context

There are several differect actors/users for the spotlight application (like non-profits, career mentors, candidates, administrators, etc.). These actors need access to different resources within the application. 

## Decision

* We will support role based access control mechanism via the auth capability microservice. THe auth capability microservice generates session tokens for users after they successfully log in. The role information is stored in the token as well as in the auth database. The auth capability microservice validates the users' roles and tokens before granting access to the resources for the users.


## Consequences

#### Positive
* Access to resources can be segmented based on user roles.
* Assigning permissions to different roles is easier. 
* More roles can be added later.
* Users can have multiple roles assigned to them if needed.

#### Negative
* Additional complexity: Adding different roles complicates the access control mechanism.
* Keeping role information and assignment up to date can cause issues.


#### Risks
* If not implemented properly then users could face issues accessing their desired resources and could loose interest.
