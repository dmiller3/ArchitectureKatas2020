#Wrinkles to Reservations
##Status
Accepted


##Context
We had to find a way to make the online order interfaces interact well with the physical pick-up locations.
We came up with a reservation system that includes some wrinkles. A reservation can be made through the website, app, or SMS.
A reservation can be applied to a food item included at a "kiosk" based location by allowing a two hour window to pick up the item.
A reservation cannot be kept at a smart fridge.
A smart fridge's customer interaction include a user pulling an item from a fridge and scanning it to purchase. This would be the time that we enforce a reservation by making the customer put the item back.
This would not be a good user experience for the smart fridge user.

An alternative to this would be a food item alert system. A user can subscribe to alerts for a food item that they want, and if that item goes out of stock before they reach the smart fridge the user will receive a notification.


##Decision
We decided to allow web interface reservations at kiosk pick up locations and the alert system at smart fridge pick up locations.


##Consequences
This creates a complication within our system to differentiate online orders from kiosk and smart fridge locations and a different (possibly confusing) user experience between the two options.
