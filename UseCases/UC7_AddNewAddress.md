UC7 – Add new address to client
==============================

Brief Description
-------------

The Client begins the process of adding a new address. 
The system requests the required data (postal address). The Client enters the requested data 
The system validates and displays the data, asking for confirmation. The Client
confirms. The system ** adds the new address to the Client ** and informs of the success of the
operation



SSD
---

![SSD_UC7.png](SSD_UC7.png)

Complete Description
----------------

### Primary actor

Client

### Stakeholders and interests

-   **Client:** wants to associate a new address with their Address list.

-   **Company:** intends that Client may request services for any of its addresses.

### Preconditions

(Be authenticated in the system as Client.)

### Postconditions

The new client address is saved in the system.

Main success scenario
----------------------------------------------

1.  The Client begins the process of adding a new address.
2.  The system requests the required data (postal address).
3.  The Client enters the requested data.
4.  The system validates and displays the data, asking for confirmation.
4.  O system valida e apresenta os dados, pedindo que os confirme.
5.  The Client confirms.
6.  The system ** adds the new address to the Client ** and informs of the success of the
operation.
    

### Exception conditions (alternative flow)

\*a. The client requests the cancellation of the registration.

>   The UC ends.

4a. Required data missing.

>   The system informs of the missing data.

>   The system allows the client to enter the missing data.(step 2)

>   2a. The client changes the data. The use case ends.

4b. The system detects that the data (or some subset of the data) entered
must be unique and already exist in the system.

>   The system alerts the Client to the fact.

>   The system allows the change. (step 2)

>   2a. The Client does not change the data. The use case ends.

4c. The system detects that the data entered (or some subset of the data)
are invalid.

>   The system alerts the Client to the fact.

>   The system allows the change. (step 2)

>   2a. The Client does not change the data. The use case ends.

### Special requirements

\-

### Variations in technologies and data

\-

### Frequency of occurrence

\-

### Open questions
-   What are the group of fields that should not be duplicated in the system?
-   Should the client have a default Address?
-   How often does this UC occur?