# Placement Management System – Salesforce

## Project Overview

The Placement Management System is a Salesforce-based application designed to manage students, job opportunities, and placement applications in one centralized system.

The project demonstrates Salesforce development concepts such as custom objects, relationships, validation rules, Apex, triggers, SOQL, asynchronous Apex, and Lightning Web Components.

## Key Features

* Student management
* Job opportunity management
* Student–Job application management
* CGPA-based job eligibility checking
* Application status tracking
* Validation rules for data accuracy
* Apex classes for business logic
* Apex triggers for application validation
* SOQL for retrieving Salesforce records
* Lightning Web Component for displaying eligible jobs
* Apply functionality for job opportunities
* Asynchronous processing using Queueable Apex

## Salesforce Objects

### Student__c

Stores student information such as:

* Student Name
* Department
* CGPA

### Job__c

Stores job opportunity information such as:

* Job Name
* Minimum CGPA
* Package
* Location
* Deadline

### Application__c

Stores student job applications such as:

* Student
* Job
* Application Status

## Technologies Used

* Salesforce
* Apex
* SOQL
* Apex Triggers
* Queueable Apex
* Lightning Web Components (LWC)
* Salesforce CLI
* GitHub

## Development Concepts

### Apex

Apex classes are used to implement reusable business logic and application services.

### Apex Triggers

Triggers are used to validate applications before they are inserted and ensure that students meet the required eligibility criteria.

### SOQL

SOQL queries are used to retrieve students, jobs, and applications from Salesforce.

### Queueable Apex

Queueable Apex is used to process background operations asynchronously.

### Lightning Web Components

LWC provides the user interface for displaying eligible job opportunities and allowing students to apply.

## Eligibility Logic

A student can apply for a job when:

`Student CGPA >= Job Minimum CGPA`

If the student's CGPA is below the required minimum CGPA, the application is prevented.

## Project Outcome

This project provided practical experience in Salesforce development, including data modeling, automation, Apex programming, asynchronous processing, and Lightning Web Component development.

## Learning Outcomes

* Understanding Salesforce data relationships
* Writing Apex classes and triggers
* Working with SOQL and DML
* Handling validation and business rules
* Implementing asynchronous Apex
* Building user interfaces using LWC
* Deploying Salesforce metadata using Salesforce CLI
* Using GitHub for project documentation and version control
