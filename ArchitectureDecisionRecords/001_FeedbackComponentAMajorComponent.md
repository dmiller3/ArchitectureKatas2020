# Feedback A Major Component

## Status
`Accepted`

## Context
The Feedback component is responsible for querying users' profile purchase history to gain meaningful feedback. The feedback could be a sub-component of the User Profile component or be separated to its first-class component in the system.

The concern is that the Feedback components could grow to be way more complicated than just getting survey results. For example, it could only send out surveys to customers who have purchased meals, provide targeted audience feedback (only vegans), or even do follow-up surveys to track satisfaction improvement. It could be responsible for sending out incentives (coupons) to increase feedback submissions or even provide recommendations based on past survey results.

The assumption is the Feedback system is going to be complex, growing, and changing over time.

If the component is a subcomponent of the User Profile component, it will cause ripple effects to the User Profile component every time it changes. The advantage is the user profile would only need to talk to the Ordering System (one channel of communication).

On the other hand, if it's a separate system, it would also separate the areas of concern. The component could change independently, but then we would have to have two communication channels. The Feedback component would have to talk to both the ordering system and User Profile component, increasing system complexity.

## Decision
Make the Feedback component a major component.

## Consequences
Feedback will need two channels of communication, the ordering system and the User Profile.

## Update
This component has now been renamed **Analytics**