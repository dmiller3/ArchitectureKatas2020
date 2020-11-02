# ChefTec manages only raw ingredients inventory

# Status
[Accepted]

# Context
Three systems have inventory management capabilities: Smart Fridge, Kiosk (Toast), and ChefTec. Smart Fridge and Toast inventory management system is more geared toward products, and ChefTec is geared more for raw ingredients.

One goal is to combine all three systems into one global inventory or make one the primary inventory system. The natural thought was to make ChefTec the primary since it does a lot more than an inventory management system, such as meal pricing, allergen information, and automatically ordering raw ingredients from vendors when stock is low. We consider ChefTec to be essential for the business.

There appears to be no existing integration between Toast or Smart Fridge to ChefTec. A note on the ChefTec website states that "CSS can Provide an Interface/integration for any System that can Import/export in ASCII Format" (https://www.cheftec.com/interfaces), which is not an ideal API interface compared to the REST API that Toast provides.

Also, we couldn't find any analytics or automation benefit if we stored
meal inventory in ChefTec. However, we see a lot of analytics for storing raw ingredients, for example: which meals can be created with the ingredients on hand or recipe modifications.

A question was raised if we should even bother store meal inventory in the ChefTec and only use it to store raw materials since the only user of this system is the Ghost Kitchen.

# Decision
Make ChefTec only manage raw ingredients.

# Consequences
Farmacy Food needs to implement a Global inventory management system from scratch that only combines meal count data from the Smart Fridges and Kiosks. The Kitchen Management component will now need to talk to the ChefTec and the newly created Global Inventory management system. One benefit of not having one of the existing systems be the primary and creating a new Inventory component is that it can be extended to accept other systems in the future.