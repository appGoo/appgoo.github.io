# appGoo

## A simple introduction

_app: noun_
short for application - "software application"

_Goo: noun_
Any sticky and viscous substance; glop, gunk: example - he fell in the goo

At its purest, appGoo is a platform for delivering browser-level code to be executed - providing that code is text based.

The majority of code sits in file systems and is retrieved to be executed, part of that execution will include getting data from a local database. Potentially it could get data from many locations, but the majority would be from a local database. By having the code near the data without having to go through additional processes of validation and connection, it would be inherently a more secure and faster process to build and then deliver the combined browser-level which is always a mixture of presentation, data and references.

As the browser-level code is generated dynamically, there is no limit on the design of how that generated code is built, it could be tailored per person or user locale - a much simpler task to achieve with generation through a procedural language rather than programs in the filesystem designed to do the same.

## What is appGoo

appGoo consists of multiple layers - the core layer which is essential for all other appGoo capability is the interpretation within the web server of a request and preparing that request into a database request to be processed. The normal treatment of the web server is to retrieve or execute a file in the filesystem. appGoo changes that concept to instead have the request served by the database. All other appGoo capability is built on top of that core concept.

Just as PHP relies on executable files to exist in the filesystem, appGoo relies on the existence of a database that has functions that process the request. The very first request that potentially could occur is authentication, and this basic requirement is also part of the appGoo core. All other functions within the database are part of subsequent layers of the appGoo development landscape that is documented below.

## appGoo Repos

appGoo is divided into 2 repositories due to the different technologies impacted. These are:

1. CORE. The base layer that exposes the most basic of capability that is required for all other subsequent layers to be built. This is the layer that allows requests from a web browser to be transformed into a database request call and the returned result is then returned to the web browser. We refer to this as the 'Core' reflecting its fundamental status and will be the first layer to be initiated.
2. SCAFFOLD. A scaffold layer allows a developer to build appGoo applications that are served from the database. This is performed via coding pgplsql files in the operating system that are then compiled into PostgreSQL functions. Assets such as css and javascript reside in the operating system in a traditional web server file delivery architecture. 
