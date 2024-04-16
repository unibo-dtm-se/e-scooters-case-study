Software Engineering @ DTM | EIT Digital - a.y. 2023-2024 

# E-Scooters Case Study - Glossary #

This doc contains the glossary of the project.

v.0.9.1-20240401

**potential user**
- a person who can create a subscription to the service
- she/he must have an age >= 14


**user**
- a person who registered to the service

**e-scooter**
- the device requested and used by users, managed and maintained by a company
can be in two different states (and which it could be in some substates)
    - in service
        - available 
            - if the battery level is >= XX 
            - if there is not a bad weather
        - not available 
            - in use
            - reserved
    - out of service 
        - need maintenance (still on street but not available)
        - in maintenance (recharging)
        - broken
        - lost
- characterising dynamic information (physical state)
    - position
    - speed
    - battery level

- renting
    - a single usage service session of an e-scooter by a  user
    - it has a start time and and end time
    - it has a start position (e-scooter start position), end position (e-scooter final position) and also the path
    - during a ride the state of the e-scooter can change, from in service to out-of- service
        - in that case, the e-scooter stops working and locks (=> need maintenance)

- e-scooter reservation
    - done by a user
    - max duration: fixed amount of minutes (30), then back to available
    - you have to pay (the same price as renting)
    - you may cancel it (but you pay the minutes)
…

- user registration 
    - first process required to become users of the service, to be done once, involving user data collection 
    - …

- billing model
    - the way in which rides are billed to users
    - the service offers two options
        - subscription-based
        - pay-per-use (minutes)
    - fixed amount for unlocking
    - …

