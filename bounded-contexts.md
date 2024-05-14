Software Engineering @ DTM | EIT Digital - a.y. 2023-2024 

# E-Scooters Case Study - Bounded Contexts Description #

This doc contains a description of the bounded contexts for the E-Scooters Case Study.

v.1.0.0-20240423

--- 

By analysing the identified subdomains and use cases, a simple design of the system accounts for three main bounded contexts:

**User Account Context**

- this bounded context concerns the  user account management subdomain  
- this context is about functionalities for:    
	- registering a new user (creating a new account)  
	- getting information about an account  
	- updating the information about  a user account    
	- getting the list of all accounts  

**Renting Context**

- this bounded context concerns the renting subdomain  
- this context is about functionalities for:  
	- starting a new rent   
	- getting information about a ongoing rent  
	- ending a rent  
	- getting the list of ongoing rents  
	
	
**E-scooter Context**

- this bounded context concerns the management and maintenance of e-scooters
- this context is about:   
	- registering a new e-scooter  
	- unlocking-for-use a registered e-scooter  
	- locking a registered  e-scooter  
	- getting information about the status of  an existing scooter  
	- getting the list of registered e-scooters  

**E-scooter Driving Context**

- this bounded context concerns e-scooter driving and control by a user doing a ride  
- this context is about:   
	- turning the e-scooter on and off
	- driving (moving, controlling speed,... etc)  
	- signaling SoS  

  


