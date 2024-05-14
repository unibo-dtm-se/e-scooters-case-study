Software Engineering @ DTM | EIT Digital - a.y. 2023-2024 

# E-Scooters Case Study - Software Architecture #

This doc contains a high level description of the software architecture of the project.

v. 1.0.0-20240513

The software architecture is designed upon the bounded contexts and the context map described in related docs.

It is composed by three main kinds of software components:

- Backend microservices  
- Frontend applications  
- Embedded system components 


**BACKEND MICROSERVICES**

The proposed architecture is based on three main backend microservices, directly mapping the identified bounded contexts and all designed upon the Ports & Adapters / Hexagonal pattern

* **Account Service** 
	- this microservice concerns the management of the accounts of the e-scooter service  
		- keeping track  of the current accounts  
		- registering a new user (account)  
		- get information about an existing account    
		-  …
	- Domain model
		- account – entity   
		- accounts – aggregate  
	- The domain model is mapped into a RESTful architecture  
		- account and accounts are represented by resources		 
	- API - RESTful model  


* **E-scooters service**
	- this microservice concerns the management of e-scooters  
		- Keeping track of the list of registered e-scooters  
	-  Domain model 
		- e-scooter dt – entity
			- properties
			- actions
			- events
		- e-scooters – aggregate  
 	- The domain model is mapped into a RESTful architecture
		- each e-scooter and e-scooters are represented as REST resources  
	- API   
		- to register a new e-scooter
		- to lookup for an existing e-scooter 
		- to access to e-scooter state (DT)  
		- to sync e-scooter DT with its physical twin


* **Renting Service**
	- this microservice concerns the management of rentings 
	- Domain model 
		- rent – entity
		- rents – aggregate
	- The domain model is mapped into a RESTful architecture
		-  each ride and rides are represented as REST resources  
	- API
		- to start a new ride  
		- to lookup for an existing ride--


**FRONT-END APPLICATIONS**

* User app
	- to register  
	- to make a new ride  
	- to show info about ongoing ride info and past rides    
	- to show possible warning/notification about the service

* E-company dashboard
	- to register a new e-scooter
	- to get information about an e-scooter
	- to monitor e-scooters map
	- to monitor ongoing rides

* Public service Dashboard
	- to display users
	- to monitor ongoing rides
	- to monitor e-scooters map

**EMBEDDED SYSTEM COMPONENTS**

- E-scooter onboard agent
	- this is a software agent running onboard the e-scooter, controlling the e-scooter and responsible of the interaction with users/maintainers
	


