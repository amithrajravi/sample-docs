## soap-vs-rest.md

# Dilemma in Choosing SOAP vs REST

In today's advanced web development world, choosing the **right web services** for your software becomes vital. Read this document to understand the fundamentals of web services, its types, and which ones to choose based on its pros and cons.


## Audience

This document is primarily focused on **Engineers** who need guidance on choosing the right web service for their applications.


## Web Services: An Overview

A web service, in simple terms, is a **communication methodology** used to exchange data between applications over the internet. The applications are built using different programming languages and run on different operating systems, but the data exchange still happens with the help of web services. Here, the **Client application** acts as a **Service Consumer** and the **Server application** acts as a **Service Provider**.

### Data Exchange

The exchange of data happens using different formats like **XML, JSON, HTML, Plain text, and so on**.

### Simple Use Case

When you search for a specific item using your Amazon mobile application, the retrieval of the item information is done using a web service.


## Types

Web services are classified into two types:

* **Simple Object Access Protocol (SOAP)** * **Representational State Transfer (REST)** 

## SOAP: An Overview

**SOAP** is an **XML-based messaging protocol**  which was designed even before REST was introduced to the web development world. The idea behind SOAP was that programs built using different programming languages and running on different operating systems can exchange structured data easily over a network. SOAP works on a variety of protocols (not just HTTP) but permits **only XML format** for data exchange.


## REST: An Overview

**REST** is an **architectural style** and **not a protocol**. An architecture is a design, which uses the existing protocol to communicate between the client and the server. REST works mostly on **HTTP**  and is **not restricted only to XML**. It permits a variety of data formats like **XML, JSON, HTML, Plain Text, and so on** for data exchange.

REST uses HTTP for the **CRUD** operations:

| Operation | HTTP Method |
| :--- | :--- |
| **CREATE** | POST  |
| **READ** | GET  |
| **UPDATE** | PUT  |
| **DELETE** | DELETE  |


## Benefits of SOAP

The following sections explain the benefits of SOAP:

### Security plays top priority

* SOAP uses **Web Services (WS) security** and is **highly reliable** compared to REST.
* The WS security specification secures SOAP services by allowing you to use **Token, Username and Password, SOAP messages encryption, and so on**.
* For instance, **banking applications** mostly rely on SOAP because of its security as it considers data privacy as a crucial factor.

### Comes with built-in retry logic

* With SOAP, during a communication failure, the **built-in retry logic** will re-initiate the failed communication.
* However, REST does not have this feature.


## Benefits of REST

The following sections explain the benefits of REST:

### JSON plays a key role

* Since **JSON** is used in the Request and Response, it becomes **lightweight, maintainable, and scalable**.
* However, SOAP uses XML that carries more bandwidth.
* JSON parses easily and provides **greater support to web browser clients**.

### Caching

* REST provides **high performance** due to **caching**.

### Ease of access

* With **HTTP** being the core for REST, the way you access the web services becomes **simpler** than SOAP.

### Multiple data formats

* REST allows data exchange through **multiple data formats** like JSON, XML, HTML, Plain text, and so on.
* However, SOAP allows **only XML** for data exchange.

### Device independent

* REST becomes a **device independent technology**. The Client consuming REST can be a TV, Mobile phone, Laptop, and so on.


## Answer to the Dilemma

Technically, the answer to this dilemma in choosing between REST or SOAP will purely depend on the **needs of your organization**, the **client types to support**, the **level of security needed**, the **flexibility you are looking for**, and so on. With that said, you can choose the one that best suits your needs based on its pros and cons.