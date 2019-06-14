# Supplementary specification

## Functionalities

-  **Safety:**
* User interactions (ie Client, Service Provider, Administrative, Human Resource Employee) must be preceded by an authentication process.
* Exceptionally some well defined features are accessible without authentication ("The use of the application by other people is restricted ...").
* All application information will have to be stored securely.
- Notification of users by email as needed.

## Usability

* The interaction between the various users and the system will have to be simple, intuitive and completely adapted to the action in question.
* Given the predictable cultural and geographical diversity of the various users of the system, it must natively support, among other things, multiple time zones and languages.
* Whenever requested by users, the application should provide a properly contextualized help / explanation for the task that the user is currently performing.
* It is essential that the interaction between users and the system is simple, intuitive and completely adapted to the action in question, considering the different players in the system and the diversity of their characteristics.

## Reliability / Reliability

* In software development it must be taken into account that it must have a very high availability rate.
* The tracking of generated and manipulated information must be guaranteed.
* It is required that the system has a minimum coverage and mutation tests (e.g. unitary, functional and integration) of 95%.

## Performance

* The system must be prepared so that the response time is roughly the same regardless of the existing load.

## Sustainability

* Company information (e.g. designation and NIF) must be specified by configuration.
* The system must also be accessible through a variety of platforms (eg PC, laptop, tablet, Windows, macOS), and its interface must adapt to the characteristics of this platform.
* The system must support different algorithms to perform the periodic allocation of service providers to the requests. Both the runtime and the algorithm to be applied must be configurable.

### Design Restrictions

* Adopt good practices in identifying requirements and analyzing and designing OO software.
* Adoption of good design practices, namely GRASP standards.
* Reuse the existing user management component in the enterprise.
* Adoption of the iterative and incremental development process.


### Implementation Restrictions

* In order to enhance interoperability with other systems already in existence and / or in development, the core of the software must be developed in Java.
* The core of software in Java.
* Adopt recognized coding standards.
* Implementation should follow a Test-Driven Development (TDD) approach.

### Interface Restrictions

--

### Physical Restrictions

--
