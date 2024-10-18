# JavaScript: Activity List

## Project Overview

This project demonstrates the use of **prototypal inheritance** in JavaScript. The goal is to implement an `Activity` class and extend it to create `Payment` and `Refund` classes using JavaScript's prototypal inheritance mechanism.

## Problem Description

You are tasked with building a basic structure to manage activities, payments, and refunds. Each type of activity holds an `amount` and other related information like `receiver` and `sender`.

### Class Descriptions

1. **Activity**
   - Represents a basic activity with an `amount`.

2. **Payment (Inherits from Activity)**
   - Represents a payment activity.
   - Properties: `amount`, `receiver`.
   - Prototype functions to handle `amount` and `receiver`.

3. **Refund (Inherits from Activity)**
   - Represents a refund activity.
   - Properties: `amount`, `sender`.
   - Prototype functions to handle `amount` and `sender`.

## Functions and Methods

### Activity
This is the base class that handles the `amount` and can be extended to other activities.

### Payment (Inherits from Activity)
This class extends the functionality of `Activity` by adding the `receiver`.

- **Constructor**:
  - `Payment(amount, receiver)`  
    Inherits `amount` from `Activity` and adds `receiver` as a new member variable.

- **Methods**:
  - `getAmount()`  
    Returns the value of `amount`.
  - `setAmount(amount)`  
    Updates the value of `amount`. Returns `true` if successful, `false` otherwise.
  - `getReceiver()`  
    Returns the value of `receiver`.
  - `setReceiver(receiver)`  
    Sets the value of `receiver`.

### Refund (Inherits from Activity)
This class extends the functionality of `Activity` by adding the `sender`.

- **Constructor**:
  - `Refund(amount, sender)`  
    Inherits `amount` from `Activity` and adds `sender` as a new member variable.

- **Methods**:
  - `getAmount()`  
    Returns the value of `amount`.
  - `setAmount(amount)`  
    Updates the value of `amount`. Returns `true` if successful, `false` otherwise.
  - `getSender()`  
    Returns the value of `sender`.
  - `setSender(sender)`  
    Sets the value of `sender`.

## Example Usage

Here is an example of how to use the `Payment` and `Refund` classes:

```javascript
// Create a Payment instance
let payment = new Payment(500, "John Doe");
console.log(payment.getAmount());  // Output: 500
console.log(payment.getReceiver());  // Output: John Doe

// Update the amount and receiver
payment.setAmount(600);
payment.setReceiver("Jane Doe");
console.log(payment.getAmount());  // Output: 600
console.log(payment.getReceiver());  // Output: Jane Doe

// Create a Refund instance
let refund = new Refund(300, "Alice");
console.log(refund.getAmount());  // Output: 300
console.log(refund.getSender());  // Output: Alice

// Update the amount and sender
refund.setAmount(350);
refund.setSender("Bob");
console.log(refund.getAmount());  // Output: 350
console.log(refund.getSender());  // Output: Bob
```

## Input Format for Custom Testing

- The first line specifies the object to be created: either `Payment` or `Refund`.
- The second line contains space-separated values representing the initial parameters:
  - For `Payment`, it includes the `amount` and `receiver`.
  - For `Refund`, it includes the `amount` and `sender`.
- The third line contains an integer representing the updated amount.
- The fourth line contains a string representing the updated `receiver` (for Payment) or `sender` (for Refund).

### Example Input

```
Payment
500 JohnDoe
600
JaneDoe
```

### Example Output

```
Payment object created with amount 500 and receiver JohnDoe
Amount updated to 600
Receiver updated to JaneDoe
Payment object details - amount is 600 and receiver is JaneDoe
Payment.prototype has property setAmount: true
Payment.prototype has property getAmount: true
Payment.prototype has property setReceiver: true
Payment.prototype has property getReceiver: true
```

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/ChickenWithACrown/activity-list.git
   ```

2. Install Node.js if you haven't already, and then run the script:
   ```bash
   node index.js
   ```

3. Provide input through stdin as described in the "Input Format" section.

## License

This project is licensed under the MIT License.
