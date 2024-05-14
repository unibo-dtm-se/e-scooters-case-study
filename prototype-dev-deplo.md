Software Engineering @ DTM | EIT Digital - a.y. 2023-2024 

# E-Scooters Case Study - Prototype Development, Deployment and Showcase#

This doc contains the description of the simple prototype and its deployment

v. 1.0.0-20240513

When moving from design to development, the first thing to do would be setting up the process and then the CI environment, before starting prototyping.

In our case, every subsystem should be managed as a separate project, with its own repo. For practical reasons, we set up 1 single project/repo with a separate directory for each subsystem. Different languages and environment can be used to develop the services and the applications. 

For simplicity, in this simple prototype we will not set up the process and the CI environment, and all services and apps will be developed in JavaScript.  Accordingly, in order to run the demo you must have ``nodejs`` and ``npm`` installed on your system.

## **Subsystems** ##


* **account-service**
	- Running on port 5050
	
* **escooter-service**
	- Running on port 5060

* **renting-service**
	- Running on port 5070 

* **user-app**
	- fragment of an hypothetical user web app, based on a web server/backend running on port 5300

* **company-dashboard**
	- fragment of an hypothetical company dashboard, based on a web server/backend running on port 5200
	
* **escooter-agent**
	- e-scooter onboard embedded software  
	- Software Agent running on port 5100 

## (Manual) **Deployment** ##

- To run the **account-service**:  
	- Open a terminal
	- change dir to ``account-service`` directory
	- type: ``npm start`` 

	You should see: ``Account service up and running - listening on port 5050``

- To run the **e-scooter-service**:  
	- Open a terminal
	- change dir to ``escooter-service`` directory 
	- type: ``npm start``

	You should see: ``E-Scooter service up and running - listening on port 5060``

- To run the **renting-service**:
	- Open a terminal
	- change dir to ``renting-service`` directory 
	- type: ``npm start`` 

	You should see: ``Renting service up and running - listening on port 5070``

- To run the **user-app**
	- Open a terminal
	- change dir to ``user-app`` directory
-- type: ``node app.js``

	You should see: ``User app backend un and running at 5300``

	To see the user app in action to register a new user, open the browswer and go to:  
	
	``http://localhost:5300/registration.html``  
	
	(try with a not existing user and with an existing user)


- To run the **company-dashboard**
	- Open a terminal
	- change dire to ``company-dashboard`` directory
	- type: ``npm start``

	You should see:``Company dashboard endpoint at 5200``

	To see the dashboard, open a new browser window and go to:
	
	``http://localhost:5200/escooters-dashboard.html``

	You should see a map (Cesena Campus)

- To run the simple **e-scooter controlling agent**
	- Open a terminal  
	- change dir to ``escooter-agent-simple`` directory
	- type: ``npm start``

For the demo we use the [Postman application](https://www.postman.com/) to directly interact with services, reproducing some use cases.  After running the application, upload the collection ``API-postman_collection.json`` available in the repo root.  The collection includes main API that can be used to emulate the case study.

Proposed demo -- sequence of requests (included in the collection API) to be done:

- get current users
- add a new user
- get again the list of users
- add an escooter
- get the list of escooters
- get the state of an escooter
- start a new rent
- get the rent info
- configure the agent to control the escooter
- turn the scooter on
- activate automode
(check the map)
- deactivate automode
- turn the scooter off
- end the rent 


## (Automated) **Deployment** ##

Docker can be used to automate the deployment. A full CI Environment  can be used to automate all the process.
