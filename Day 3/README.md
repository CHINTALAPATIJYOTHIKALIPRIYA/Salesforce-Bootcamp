
# Salesforce Bootcamp Day 3 – Validation Rules, Flows & Triggers

## Overview

In Day 3 of the Salesforce Developer Bootcamp, I enhanced the Placement Management System by implementing declarative automation using Validation Rules and Record-Triggered Flows.

The main objective was to understand when to use Validation Rules, Flows, and Apex Triggers based on business requirements.

## Concepts Learned

### Validation Rule

Validation Rules are used to enforce data quality by preventing users from saving records when specific conditions are not satisfied.

Example:

* Preventing applications when a student's CGPA is below the required minimum CGPA.
* Preventing invalid application dates.

### Flow

Flow is a Salesforce automation tool used to automate business processes without writing code.

Used for:

* Automatically updating fields.
* Sending email notifications.
* Creating related records.

### Apex Trigger

Apex Trigger is used when complex automation cannot be achieved using declarative tools like Flow.

Used for:

* Complex business logic.
* Large data processing.
* Advanced calculations.

## Automation Design Decisions

| Requirement                   | Solution Used          | Reason                                                   |
| ----------------------------- | ---------------------- | -------------------------------------------------------- |
| Reject duplicate applications | Validation Rule / Flow | Prevent invalid duplicate submissions                    |
| Auto-fill Application Date    | Record-Triggered Flow  | Automatically populate date when application is created  |
| Send Email Notification       | Flow                   | Email automation can be handled declaratively            |
| Reject low CGPA applications  | Validation Rule        | Prevent saving invalid records                           |
| Create Offer Letter record    | Flow                   | Automatically create related records after status change |

## Record-Triggered Flow Implementation

Created a Record-Triggered Flow on the Application object.

### Flow Features:

* Automatically sets Application Date when a new application is created.
* Sends confirmation email notification to the Placement Officer.
* Executes automatically when application records are created.

### Flow Elements Used:

* Start Element
* Assignment Element
* Email Action
* Decision Element (if required)

## Validation Rules Created

### 1. Student CGPA Validation

Purpose:
Ensure student's CGPA meets the minimum CGPA requirement for a job.

Logic:

* Compare Student CGPA with Job Minimum CGPA.
* Prevent application submission if requirements are not satisfied.

### 2. Application Date Validation

Purpose:
Prevent applications after the job closing date.

Logic:

* Application Date should not be greater than Job Closing Date.

### 3. Mandatory Field Validation

Purpose:
Ensure required application details are completed before saving.

## Flow vs Trigger Understanding

Flow is preferred when:

* Standard automation is required.
* Field updates, emails, and record creation are needed.

Apex Trigger is preferred when:

* Complex logic is required.
* Multiple objects need advanced processing.
* External integrations are involved.

## Debugging Automation

Problem:
If Trigger, Flow, and Workflow all update the same field, automation conflicts and repeated execution can occur.

Solution:

* Avoid duplicate automation.
* Use a proper automation strategy.
* Prefer Flow for simple requirements and Apex only when necessary.

## Key Learning Outcomes

* Difference between Validation Rules, Flows, and Apex Triggers.
* Building Record-Triggered Flows.
* Designing Salesforce automation solutions.
* Choosing the right automation tool for business requirements.
* Improving data quality using validation rules.

## Project Enhancement

Enhanced Placement Management System with:

* Record-Triggered Flow for Application Date automation.
* Email notification automation.
* Validation Rules for data quality.
* Automated business process handling.

## Tools Used

* Salesforce Lightning Platform
* Flow Builder
* Object Manager
* Validation Rules
* Trailhead Learning Modules

## Conclusion

This assignment improved my understanding of Salesforce declarative automation and helped me design solutions similar to real-world Salesforce Developer scenarios.
