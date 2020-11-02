# Event-Based Architecture as the System Architecture
## Status
`Superseded`

## Context
We considered an event-based architecture as our system because of an emphasis on scalability within the project prompt.

When developing a system architecture following a event-based structure, we settled on a hybrid event and request messages with broker topology.
A mediator topology was not used due to no use of a strong workflow because a lot of our processes are passing instructions to 3rd party utilities.
The services we were deploying also used a lot of shared data which creates a "ball of mud" architecture because a lot of services need to talk to a lot of services when they could be routed through a shared resource.

## Decision
Use a service architecture over an event-based architecture.

## Consequences
We lose a bit of user responsiveness but ultimately receive a data coherency boost due to the service architecture.
