# Library Management System

## Overview
This is a simple library management system implemented using Hibernate for data persistence.

## Entities
1. **Author:**
    - Attributes: id (Primary Key), name, country
    - Relationship: One author can have multiple books.
    - Annotations: @Entity, @Id, @GeneratedValue, @OneToMany(mappedBy = "author", cascade = CascadeType.ALL)

2. **Book:**
    - Attributes: id (Primary Key), title, publicationYear, price
    - Relationship: Many books can be written by one author.
    - Annotations: @Entity, @Id, @GeneratedValue, @ManyToOne, @JoinColumn(name = "author_id")

## Operations Implemented
1. Retrieve all books published after the year 2010.
2. Update the price of all books published by a specific author by 10%.
3. Delete an author and cascade the deletion to all associated books.
4. Find the average price of all books.
5. Retrieve all authors along with the count of books they have written.
6. Retrieve books written by authors from a specific country using named parameters.

## Project Setup
- Ensure you have MySQL installed and running.
- Create a database named `library_db`.
- Update `hibernate.cfg.xml` with your MySQL username and password.
- Run the application.

## Running Tests
Tests are located in `LibraryRepositoryTest.java`. You can run them using your preferred IDE or build tool.

## Dependencies
- Hibernate
- MySQL Connector
- Spring Data JPA

