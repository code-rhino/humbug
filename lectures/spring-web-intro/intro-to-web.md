# Java and the web


-
-
# What is REST?
* REST stands for **RE**presentational**S**tate **T**ransfer and is an architectural
style for designing distributed network applications
* More precisely, **REST** is an architectural style consisting of a coordinated set
of architectural constraints applied to components, connectors, and data
elements, within a distributed hypermedia system.

-
-

# Client-Server

Concerns should be separated between clients and servers. This enables

-
-
# Stateless



-
-
# Layered System



-
-
# Cache



-
-
# Uniform Interface





-
-

# Code on demand

Clients can extend their functionality by downloading and executing code on demand. Examples include JavaScript scripts, Java applets, Silverlight,and so on. This is an optional constraint.

-
-

# URI

Uniform Resource Identifier, or URI, for uniquely identifying resources.

-
-

# URI Templates

* Resource links can be dynamic

-
-

# Representation



-
-

# HTTP Method (GET)

The GET method is used to retrieve information from the given server using

-
-

# Idempotency


* HTTP methods such

-
-

# HTTP Methods (POST)



-
-

# HTTP Methods (HEAD)



-
-

# HTTP Methods (PUT)

Replaces all current representations of the target resource with the uploaded content.

-
-

# HTTP Methods (DELETE)



-
-

# HTTP Methods (CONNECT)

Establishes a tunnel to the server identified by a given URI.

-
-
# HTTP Methods (OPTIONS)



-
-

# HTTP Methods (TRACE)

Performs a message loop-back test along the path to the target resource.

-
-

# CRUD

* Create

-
-

# HTTP Status Codes


* 2xx Success (200 OK)
* 3xx Redirection (300 Multiple Choices)

* 5xx Server Error (500 Internal Server Error)

-
-

# HTTP Status Codes

# (1xx Informational)





This means that the server has received the request headers, and that the client should

-



This means the requester has asked the server to switch protocols and the server is

-





-
-

# HTTP Status Codes



-

# 200 OK

Standard response for successful HTTP requests.

# 201 CREATED

The request has been fulfilled and resulted in a new resource being

# 202 Accepted

The request has been accepted for processing, but the processing has not

-
-

# HTTP Status Codes


300 Multiple Choices

# 301 Moved Permanently

This and all future requests should be directed to the given URI

# 308 Permanent Redirect

The request, and all future requests should be repeated using another URI.

-
-

# HTTP Status Codes

# (4xx Client Error)

# 400 Bad Request

The server cannot or will not process the request due to something

# 401 Unauthorized

Similar to 403 Forbidden, but specifically for use when authentication

# 404 Not Found

The requested resource could not be found but may be available

-
-

# WEB Socket

A protocol providing full-duplex communication channels over a single TCP

-
-

# Servlet




-
-

# AOP



-
-

# ORM

Object-relational mapping (ORM) is a technique (a.k.a. design pattern) of

-
-

# JMS

**JMS** is a part of the Java Platform, Enterprise Edition, and is defined by a

-
-

# Transaction

In computer programming, a transaction usually means a sequence of

-
-

# BEAN

A bean is an object that is instantiated, assembled, and otherwise managed

-
-

# IOC

In software engineering, inversion of control (IoC) describes a design in

-
-

# Dependency Injection (DI)

