# Sprint 8 – Asynchronous Apex

## Objective

In this sprint, I learned how Salesforce handles background processing using Asynchronous Apex.

The main goal was to understand when work should happen immediately and when it can be moved to the background.

## Concepts Covered

### 1. Synchronous vs Asynchronous Processing

Synchronous processing means the user waits for the transaction to complete.

Asynchronous processing allows Salesforce to execute suitable work in the background, improving the user experience.

### 2. Future Methods

Future Methods are used to execute eligible Apex code asynchronously.

```apex
@future
public static void processApplication(Id applicationId) {
    System.debug('Processing application asynchronously');
}
