# Automated Ticketing System
This system is built for onlin food delivery compnay. Which will go scan the system and create the tickets so hired agent will be able to
resolve the ticket even before customer reports.
monitor the deliveries and create the ticket, Calculate the
priority of each ticket by taking into consideration the above factors.

###Requirments
    . JDK 1.8
    . Maven 3

###Running the application locally

There are several ways to run a Spring Boot application on your local machine. One way is to execute the main method
in the com.callsign.exercise.automatedticketingsystem.AutomatedTicketingSystemApplication class from your IDE.
Alternatively you can use the Spring Boot Maven plugin like so:

    mvn spring-boot:run

---
##User Guide

###API DOCUMENTATION

- Authentication APIs

|APIs                     |Description                       |
|--------------------------------|---------------------------------|
|POST /auth/login| Use to login the user and return a JWT Token|
|POST /auth/signup | User to Signup a new user and save record in DB


- Tikcets APIs

|APIs                     |Description                       |
|--------------------------------|---------------------------------|
|GET /ticket/| Get all the tikcet according to the priority|

---

##Project Details

Delivery Parameter

    1. Delivery ID
    2. Customer Type (VIP, Loyal, New)
    3. Delivery Status (Order received, Order Preparing, Order Pickedup, Order Delivered)
    4. Expected time of delivery
    5. The current distance from the destination
    6. Rider rating.
    7. Restaurant Mean time to prepare food.
    8. Time to reach the destination

Ticket Report when

>Estimated Delivery Time =  Mean time to prepare food + Time to reach the destination

>Estimated Time is greater then the expected time report a ticket
and raise a ticket if your estimation is greater than the
expected time

Ticket Priority

>1. Expected time of delivery is passed and not delivered
> 2. Customer has "VIP" Status

e from youtube and different documentation.
