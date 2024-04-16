Software Engineering @ DTM | EIT Digital - a.y. 2023-2024 

# E-Scooters Case Study - Use Cases #

This doc contains the glossary of the project.

v.0.9.1-20240401

This doc contains a description of the use cases of the project.

v. 0.9.1-20240401

### Use Case Descriptions ###

**Create Account** 

Main Success Scenario:

1. User fills a registration form with basic info (Name, Surname, email, username, pwd, ccard
2. User submits the registration form
3. System confirms the registration
4. System sends a confirmation e-mail to user

Extensions:

3a. Registration fails  
.1: User may reenter the info
  

**Visualise Account**

Main Success Scenario:

1. User logins 
2. System shows accounts info
3. User logouts 

**Update Account**

Main Success Scenario:

1. User logins 
2. User updates account info
3. User logouts 

**Rent an E-scooter**

Main Success Scenario:

1. User requests to use an e-scooter

    – by scanning a QR code on the e-scooter. This can be done with any QR code scan app or with the e2-scooter app

    – selecting the e-scooter on the map 

2. [in the case that the user has the app] 
    System accepts the request and unlocks the e-scooter 
3. User rides e-scooter 
4. User notifies the end of renting
5. System bills for the ride, according to user billing model

Extensions:

2a. System does not grant the request
.1: User may reenter the request

2b. The user does have installed the app => after scanning the QR code, the user is redirected to web page that suggests to download and install the app

**Reserve an E-scooter**

Main Success Scenario:

1. User requests to reserve an e-scooter
   
    – selecting the e-scooter on the map (you don't need to scan the QR code) 
    
2. System accepts the request and does the reservation, changing the state of the e-scooter
3. User unlocks the reserved e-scooter (in time) 
     → renting scenario + billing the reservation time

Extensions:
3a. User does not unlock the the reserved e-scooter on time
.1: The system cancels the reservation and bill the reservation time

3b. User cancels the reservation
.1: The system cancels the reservation and bill the reservation time

**Monitor Rides**

Main Success Scenario:

1. Company logins
2. System shows current rides on a map
3. Company selects a ride
4. System shows details about the selected ride

Extensions:
...

**Analyse Rent Stats**

Main Success Scenario:

1. Company logins
2. Company shows statistics about rides

Extensions:
...

**Visualise Rent User History**

Main Success Scenario:

1. User logins 
2. User visualises the history of past rents
3. User logouts 

Extensions:
...

**Mainstain E-scooters** 

Main Success Scenario:

1. Company identifies the set of e-scooter (out of service) to be collected 
    (using some policy, that could be adapted according to the need)
2. For every identified e-scooter, Company collects it
2. Company performs a check-up / recharge of the e-scooter 
3. Company re-deploy the e-scooter in a station, making it available

Extensions:
...

**Monitor E-scooters**

Main Success Scenario:

1. Company logins
2. System shows current position of e-scooters on a map
3. Company selects an e-scooter
4. System shows details about the selected e-scooter 
5. Company logouts

Extensions:
...

**Drive E-scooter**

Main Success Scenario:

1. User turns on the e-scooter
2. User drives the e-scooter
3. User turns off the e-scooter

Extensions:
...

### Use Case Diagram ###

![Use Case Diagram](https://github.com/unibo-dtm-se/e-scooters-case-study/blob/main/use-cases.png)

