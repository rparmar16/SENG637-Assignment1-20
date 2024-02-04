# Testing Plan ATM System – Lab 1 Version SUT V1.0/1.1

## Introduction

Group Number : 20
| Group Member Name|
|------------------|
|Robby|
|Gopal|
|Jubayer|
|Usman|
|Ehsan|

This Test Plan has been established to highlight the scope, methodology, for all testing work undertaken for the ATM simulation system. It delineates the items and features slated for testing such as types, strategy and scope for testing, logistics, comparison between exploratory & manual testing, and notes during peer reviews.

## Test Types & Strategy:

The test plan for Manual Non Scripted testing will prioritize all key operations & functions of the ATM SUT V1.0. The key areas, functions & operations that the Manual Non Scripted testing will be following as listed below, which are expected to be used by either users & operators:

1. ATM Operator Panel Functions And Logging
1. Card PIN validation and PIN verification
1. Transactions:
   1. Cash withdrawal
   1. Deposit processing
   1. Money transfer
   1. Balance inquiry
1. Transaction cancellation
1. Communication with the bank
1. Receipt Generation & Display
1. User interface
1. Operator functions (start/stop, cash verification, log entries)
1. Access to shared accounts & transactions

The key components for the testing environment will be following as listed below:

1. ATM Simulation V1.0 is the SUT
1. Available cards & PINs:
   1. Card 1, PIN 42
   1. Card 2, PIN 1234
1. Initial Holding Balance of Cards
   1. Card 1
      1. Chequing (Shared): $100
      1. Savings: $1000
   1. Card 2
      1. Chequing (Shared): $100
      1. Savings: $1000
      1. Money Market: $5000
1. Diversified testing data:
   1. Various amounts of withdrawal, deposit, transfer amounts
   1. Balance inquiries on different accounts
1. Banking communication & system networking

## Scope of Testing:
For each of the key operations, functions and areas for SUT defined above, the following strategy is defined for the Manual Non Scripted testing. Common paths and exceptional paths are defined within the cases.

**Operator Panel:**

1. Test on/off operation of ATM and logging (common)

**Card Validation:**

1. Test available Card (1 and 2) (common)
1. Test invalid Cards 
1. Test invalid PINs
1. Test valid Cards with Invalid PINs and valid PINs after unsuccessful PINs

**Transactions:**

1. *Deposits:*
   1. Test various amount for deposits (common)
   1. Test deposits in multiple accounts (common)
   1. Confirm receipt & log details with deposits (common)
1. *Withdrawals:*
   1. Test different amounts for withdrawals (common)
   1. Test withdrawals in all accounts (common)
   1. Confirm with receipt and SUT log (common)
   1. Withdraw invalid amounts exceeding balance (exceptional)
1. *Transfer:*
   1. Test transferring between different accounts and ensure all account have transferred from and to (common)
   1. Transfer invalid or insufficient amounts (exceptional)
   1. Transfer to invalid accounts (exceptional)
1. *Balance Inquiry*
   1. Test balance reporting of all valid accounts (common)
   1. Test balance reporting of invalid accounts (exceptional)
   1. Confirm receipt and log verification with balance inquiries (common)
1. *Transaction Operations:*
   1. Confirm transaction cancel, continue and ejection operations for different stages (common)
1. *User Interface:*
   1. Test all operations and buttons on the user interface for different SUT pages (exceptional)
   1. Test output of different operations in the display and receipts (exceptional)
1. *Receipts:*
   1. Confirm receipt data is validated with system log (exceptional)
   1. Confirm receipt displays correct information for the transactions (common)
  
## Test Logistics

Assign different groups different components to test

### Deposits:
- Usman
- Jubayer
- Ehsan

### Withdrawals:
- Robby
- Gopal

### Transfer:
- Usman
- Jubayer
- Ehsan

### Balance Inquiry:
- Robby
- Gopal

### Transaction Operations:
- Usman
- Jubayer
- Ehsan

### User Interface:
- Robby
- Gopal

### Receipts:
- Usman
- Jubayer
- Ehsan










## Testing Execution & Reposting of Issues

To execute testing of the testing cases, each of the above test cases will be followed (with different team members executing different cases). Test data will be prepared using valid data and invalid data for card numbers, PIN, different deposit amounts, withdrawal amounts, transfer amounts and communication with the bank for various transactions.

All cases will be individually and thoroughly tested for diversified valid & invalid data. Results will be compared for expected outcome vs. actual outcome for all of the test cases and cases where there are issues identified will be collected & reported as defects. Detailed conditions, data utilized, SUT, priority and steps to reproduce the issues & bugs will be reported in the tracking tool.

## Comparison of Exploratory and Manual Functional Testing

To provide a comprehensive comparison between exploratory testing and manual functional testing based on the provided test suite, we will examine various aspects such as benefits, trade-offs, effectiveness, and efficiency. The test suite provided outlines a series of manual functional tests for an ATM system, covering a wide range of scenarios from system startup and shutdown to transactions like deposits, withdrawals, and transfers, as well as error handling and user input validation.

**Benefits**

**Manual Functional Testing (Based on the Test Suite):**

- **Precision and Coverage:** The provided test suite meticulously outlines specific test cases, ensuring thorough coverage of all the system functionalities and user interactions. This ensures that each aspect of the system is tested under defined conditions, leading to a comprehensive evaluation of the system's behavior.
- **Predictability:** With a predefined set of inputs and expected outputs, it offers a clear benchmark for correctness, facilitating straightforward assessment of the system's performance and behavior.
- **Documentation:** Serves as detailed documentation for testing procedures and expected system behavior, which is useful for onboarding, training, and reference.

**Exploratory Testing:**

- **Flexibility:** It allows testers to adapt and explore the system dynamically, identifying issues that may not be covered by the initial test suite. This flexibility can uncover unexpected bugs or usability issues.
- **Creativity and Insight:** Testers can apply their understanding and intuition about the system, potentially identifying more subtle or complex issues than what scripted testing might reveal.
- **Efficiency in Unfamiliar Domains:** Particularly useful in early stages of development or when dealing with complex, unpredictable systems where defining a comprehensive test suite upfront is challenging.

**Trade-offs**

**Manual Functional Testing:**

- **Time-Consuming:** Executing the test suite manually can be labor-intensive and time-consuming, especially as the number of test cases grows.
- **Limited by Script:** Testers are limited to the scenarios outlined in the test suite, potentially missing out on unexpected behaviors or edge cases not considered in the test design.

**Exploratory Testing:**

- **Lack of Coverage Guarantees:** Without a structured test suite, some parts of the application might be under-tested, leading to gaps in coverage.
- **Difficulty in Reproducibility:** Issues found during exploratory testing can sometimes be harder to reproduce due to the less structured nature of the testing approach.

**Effectiveness**

**Manual Functional Testing:**

- Highly effective for verifying known, specific scenarios and ensuring that the application behaves as expected in those scenarios.
- Essential for regression testing, ensuring that new changes do not break existing functionality.

**Exploratory Testing:**

- Highly effective in finding new, unforeseen bugs and exploring how the system behaves under less predictable scenarios.
- Complements manual functional testing by covering aspects that are hard to anticipate and script in advance.

**Efficiency**

**Manual Functional Testing:**

- Efficiency can be hampered by the repetitive nature of executing manual test cases, especially for large test suites.
- Automation of manual tests can enhance efficiency, though the initial test suite provides a solid foundation for such automation.

**Exploratory Testing:**

- Can be more efficient in early stages of development or for complex systems where defining a complete test suite upfront is not feasible.
- Allows for quick, iterative testing focused on discovery and learning about the system's behavior in real-time.

In conclusion, both exploratory and manual functional testing offer distinct advantages and play crucial roles in a comprehensive testing strategy. Manual functional testing, based on a predefined test suite like the one provided, ensures thorough coverage and reliability testing for known scenarios. Exploratory testing, on the other hand, excels in identifying unexpected issues, leveraging tester intuition and adaptability. A balanced approach, integrating both methods, typically yields the best outcomes, ensuring both breadth and depth of testing.

## Notes & Discussions
In our two groups, we worked on the software issues in different ways. Group 1, with Jubayer, Usman, and Ehsan, looked at the technical side. They were worried about problems happening again and again, like the balance inquiry issue and the tricky PIN process. They thought these were not just small mistakes but bigger troubles in the system. They wondered if the errors in taking out money were because the system didn't check the account balance properly or if there was a mistake in how the updates were done. They suggested digging deep into how the system checks transactions.

Now, Group 2, with Robby and Gopal, cared more about how these problems affected users and the overall operation. They were bothered that basic things like checking balances or printing receipts had errors, which could make customers lose trust and cause problems for the bank. They said it's not just about fixing the problems but also making sure all account types are thoroughly tested to stop such issues. They emphasized that clear communication and accurate transaction records are crucial to keep customers happy and make the bank work smoothly.

## Reflection and Learning
### Difficulties and Challenges
While tackling this assignment, we smoothly handled different tasks, and things went quite well overall. Yet, figuring out how Jira works took some getting used to. Understanding all the details of the Jira platform required a bit of time and effort. Another challenge was assigning tasks among team members effectively, affecting the assignment's overall efficiency. To improve in the future, we plan to tackle these challenges early on and become more familiar with Jira, aiming for smoother task delegation and better collaboration in upcoming assignments.


### Comments and feedback
The SENG 637 Lab Assignment #1 is a great way to learn about software testing step by step. It covers exploring a system, trying out different testing methods, and checking if issues are fixed in a new version. The use of tools like Jira and Azure DevOps adds a real-world touch. The guidelines for submitting work are clear, and the lab encourages working in pairs, enhancing learning through teamwork. The document is easy to follow, with simple language and helpful feedback sections. Overall, it's a practical and well-organized introduction to software testing.

