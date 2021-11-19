# PeanutDB

An inheritance based embedded database.

## What is the goal of this database?

Many projects make use of inheritance to prevent duplicate code, and also as a form of polymorphism. Storing these polymorphic types in a database can be difficut as you either have to have tables for each subtype, one table with nullable columns, or has one type relations to hold the extra data. I dont think that any of these are acceptable and should be abstracted out. This project will allow you to define tables that extend others, and enable you to use polymorphism in your queries.

## Embedded DB?

I'm firstly going to build this project as an embedded database for the MVP but have the goal to expand it to be a fully fleged database system supporting multiple concurrent queries.

## Application Structure

I'm using the Law of Demeter as a design principle because it enables incrimental changes to small parts of the application without drastic overall refactoring.

### Frontend

The fronted will expose the public interface and will interact with mediary interfaces.

### Backend

The backed will be responsible for storing and reading data from a persistant location. The MVP backend will utilize a JSON file as this is easy to implement. Obviously this is not ideal but should make inital proof of concept implementation easier.
