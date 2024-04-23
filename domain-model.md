Software Engineering @ DTM | EIT Digital - a.y. 2023-2024 

# E-Scooters Case Study - Domain Model #

This doc contains the description of the domain model of the E-Scooters project.

v. 1.0.0-20240401

--- 

The domain model is an object model of the E-Scooters domain, based on the Ubiquitous Language identifying the knowledge crunching and strategic design stage.

- **User Account** Entity
	- this entity models a user account of the E-Scooter service
	- It keeps track of User data
- **User Accounts** Aggregate  
	- this aggregate models the set of user accounts registered to the E-Scooters service, providing functionalities for registering a new user account, searching for a user given its identifier, etc.  
- **EScooter** Entity  
	- this entity models an E-Scooter, keeping track about its state and providing functionalities for its management (e.g., locking, unlocking,..) 
- **EScooters** Aggregate
	- this aggregate models the set of e-scooters available in the E-Scooters service, providing functionalities for registering/removing an e-scooter, for searching for a-scooter given its identifier, etc.
- **Rent** Entity
	- this entity models a ongoing rent of an e-escooter by a user, including when the rent started.
- **Rentings** Aggregate  
	- this aggregate models the set of ongoing rentings 


## UML Class Diagram ##

![UML Domain Model Diagram](https://github.com/unibo-dtm-se/e-scooters-case-study/blob/main/domain-model-UML.png)



