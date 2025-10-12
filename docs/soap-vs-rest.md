## soap-vs-rest.md

# Dilemma in Choosing SOAP vs REST

In today's advanced web development world, choosing the **right web services** for your software becomes vital[cite: 2]. Read this document to understand the fundamentals of web services, its types, and which ones to choose based on its pros and cons[cite: 3].

***

## Audience

This document is primarily focused on **Engineers** who need guidance on choosing the right web service for their applications[cite: 5].

***

## Web Services: An Overview

A web service, in simple terms, is a **communication methodology** used to exchange data between applications over the internet[cite: 7]. The applications are built using different programming languages and run on different operating systems, but the data exchange still happens with the help of web services[cite: 8]. Here, the **Client application** acts as a **Service Consumer** and the **Server application** acts as a **Service Provider**[cite: 9].

### Data Exchange

The exchange of data happens using different formats like **XML, JSON, HTML, Plain text, and so on**[cite: 10].

### Simple Use Case

When you search for a specific item using your Amazon mobile application, the retrieval of the item information is done using a web service[cite: 12].

***

## Types

Web services are classified into two types[cite: 14]:

* **Simple Object Access Protocol (SOAP)** [cite: 15]
* **Representational State Transfer (REST)** [cite: 15]

***

## SOAP: An Overview

**SOAP** is an **XML-based messaging protocol** [cite: 17] which was designed even before REST was introduced to the web development world[cite: 17]. The idea behind SOAP was that programs built using different programming languages and running on different operating systems can exchange structured data easily over a network[cite: 18]. SOAP works on a variety of protocols (not just HTTP) but permits **only XML format** for data exchange[cite: 19].

***

## REST: An Overview

**REST** is an **architectural style** and **not a protocol**[cite: 22]. An architecture is a design, which uses the existing protocol to communicate between the client and the server[cite: 22]. REST works mostly on **HTTP** [cite: 23] and is **not restricted only to XML**[cite: 23]. It permits a variety of data formats like **XML, JSON, HTML, Plain Text, and so on** for data exchange[cite: 24].

REST uses HTTP for the **CRUD** operations[cite: 25]:

| Operation | HTTP Method |
| :--- | :--- |
| **CREATE** | POST [cite: 26, 27] |
| **READ** | GET [cite: 28] |
| **UPDATE** | PUT [cite: 29] |
| **DELETE** | DELETE [cite: 30] |

***

## Benefits of SOAP

The following sections explain the benefits of SOAP[cite: 32]:

### Security plays top priority

* SOAP uses **Web Services (WS) security** and is **highly reliable** compared to REST[cite: 34].
* The WS security specification secures SOAP services by allowing you to use **Token, Username and Password, SOAP messages encryption, and so on**[cite: 35].
* For instance, **banking applications** mostly rely on SOAP because of its security as it considers data privacy as a crucial factor[cite: 36].

### Comes with built-in retry logic

* With SOAP, during a communication failure, the **built-in retry logic** will re-initiate the failed communication[cite: 38].
* However, REST does not have this feature[cite: 39].

***

## Benefits of REST

The following sections explain the benefits of REST[cite: 41]:

### JSON plays a key role

* Since **JSON** is used in the Request and Response, it becomes **lightweight, maintainable, and scalable**[cite: 43].
* However, SOAP uses XML that carries more bandwidth[cite: 44].
* JSON parses easily and provides **greater support to web browser clients**[cite: 45].

### Caching

* REST provides **high performance** due to **caching**[cite: 47].

### Ease of access

* With **HTTP** being the core for REST, the way you access the web services becomes **simpler** than SOAP[cite: 49].

### Multiple data formats

* REST allows data exchange through **multiple data formats** like JSON, XML, HTML, Plain text, and so on[cite: 51].
* However, SOAP allows **only XML** for data exchange[cite: 52].

### Device independent

* REST becomes a **device independent technology**[cite: 54]. The Client consuming REST can be a TV, Mobile phone, Laptop, and so on[cite: 54].

***

## Answer to the Dilemma

Technically, the answer to this dilemma in choosing between REST or SOAP will purely depend on the **needs of your organization**, the **client types to support**, the **level of security needed**, the **flexibility you are looking for**, and so on[cite: 56]. With that said, you can choose the one that best suits your needs based on its pros and cons[cite: 57].