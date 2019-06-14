# CS 493 - Cloud Application Development
Final Project for CS 493, created with GitHub Classroom.

## Tarpaulin Introduction
Tarpaulin, a lightweight course management tool that’s an “alternative” to Canvas.  In particular, Tarpaulin allows users (instructors and students) to see information about the courses they’re teaching/taking.  It allows instructors to create assignments for their courses, and it allows students to submit solutions to those assignments.
The Tarpaulin API supports all of the endpoints as described in the [Tarpaulin OpenAPI Specification](https://gist.github.com/robwhess/ec734c97a98868dbc1776718cd73b203). 
This API was developed using **NodeJS** and **MongoDB** as the backend database. 

## Tarpaulin API Entities
Below is a list of the entities that the Tarpaulin API suppports:
- **Users**: these represent Tarpaulin application users.  Each User can have one of three roles: admin, instructor, and student.  Each of these roles represents a different set of permissions to perform certain API actions.  The permissions associated with these roles are defined further in the Tarpaulin OpenAPI specification.
- **Courses**: these represent courses being managed in Tarpaulin.  Each Course has basic information, such as subject code, number, title, instructor, etc.  Each Course also has a list of enrolled students (i.e. Tarpaulin Users with the student role) as well as a set of assignments.  More details about how to manage these pieces of data are included both below and in the Tarpaulin OpenAPI specification.
- **Assignments**: these represent a single assignment for a Tarpaulin Course.  Each Assignment has basic information such as a title, due date, etc.  It also has a list of individual student submissions.
- **Submissions**: these represent a single student submission for an Assignment in Tarpaulin.  Each submission is tied to the student who submitted it and marked with a submission timestamp.  Each submission is associated with a specific file, which will be uploaded to the Tarpaulin API and stored, so it can be downloaded later.

## Concepts Learned
- API Architecture Design and Implementation
- API Endpoint Pagination
- Development within Docker Environment
- IP Addressed based Rate Limiting
- CSV Implementation from GET request 
- User Authentication and Authorization using Json Web Tokens (JWT)
