# Overview

> oBIX is designed to provide access to the embedded software systems which sense and control the world around us.  
> oBIX Version 1.1, Working Draft 06, 08 June 2010 

oBIX is expected to help improve operational efficiencies for end-users by bridging the gap between facility systems and enterprise applications. Facility operators, building owners, and tenants will be able to make decisions based on a comprehensive view of their enterprise including lifecycle costs, environmental considerations, operations, and other performance factors.

## Normalization
Version 1.0 of oBIX provides a normalized representation for three of these:

- __Points__: representing a single scalar value and its status - typically these map to sensors, actuators, or configuration variables like a setpoint;
- __Histories__: modeling and querying of time sampled point data. Typically edge devices collect a time stamped history of point values which can be fed into higher level applications for analysis;
- __Alarming__: modeling, routing, and acknowledgment of alarms. Alarms indicate a condition which requires notification of either a user or another application.

## Architecture
The oBIX architecture is based on the following principles:

- **Object Model**: a concise object model used to define all oBIX information
- **XML Syntax**: a simple XML syntax for expressing the object model
- **URIs**: URIs are used to identify information within the object model
- **REST**: a small set of verbs is used to access object via their URIs and transfer their state via XML
- **Contracts**: a template model for expressing new oBIX "types"
- **Extendibility**: providing for consistent extendibility using only these concepts

## Operations
Operations are the things that you can "do" to an oBIX object. They are akin to methods in traditional OO languages. Typically they map to commands rather than a variable that has continuous state.

All operations take exactly one object as a parameter and return exactly one object as a result. The **in** and **out** attributes define the contract list for the input and output objects.

I have illustrated how to invoke these operations by Postman, you can refer to [obix_intro.docx](https://github.com/hanshu/obix/blob/master/obix_intro.docx?raw=true) for detailed information.

## References
- [obix.postman_collection](https://github.com/hanshu/obix/blob/master/obix.postman_collection.json)  
    I export from my Postman for your testing, and provide [Document oBIX APIs on Postman Cloud](https://documenter.getpostman.com/view/1068428/S1LpaXea) for your reference.