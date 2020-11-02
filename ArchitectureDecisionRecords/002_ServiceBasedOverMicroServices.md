# Service Architecture Over MicroServices

## Status
`Accepted`

## Context

The main architecture could be a Service or Microservice arcitecture.

The microservices architecture is a candidate because the system can be separated into distinct sections targeted at a specific uses,
such as User services, Ordering services, and Financial services. However, the communication and integration between these areas or services
makes it challenging to decouple the domains, services, and data. For example, the Order service and User service might communicate to determine
relevant offers and validate whether a use can give feedback on a product (depending on whether the user actually purchased the product).
The Order service and Kitchen Management service might communicate to update prices and relay which meals are out of stock or in demand. Data
(specifically data related to user profiles and needs) is unique to this product and experience, so service based architecture is a more natural fit.
It will allow a "share-as-much-as-possible" approach, rather than the microservices "share-as-little-as-possible" approach.

## Decision
Use a Service Architecture over a Microservices Architecture.

## Consequences
Data will be easily accessible across our components, allowing Farmacy Foods to integrate their various tools into a cohesive system. However, these components will be more tightly coupled. They will be more vulnerable to the risks associated with changing a single component or database, especially if connected to many others.
