**Exploratory (Manual Non-scripted) Testing Plan ATM SUT V1.0**

## Introduction:

This Test Plan is crafted to specify the scope, methodology, for all testing work undertaken for the ATM simulation system. It delineates the items and features slated for testing, the testing methodologies to be applied, assigns testing responsibilities to members, outlines the resources and schedule necessary for testing completion, and addresses the potential risks linked to the plan.

## Test Strategy:

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

## Testing Strategy & Cases:
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

## Testing Execution & Reposting of Issues:

To execute testing of the testing cases, each of the above test cases will be followed (with different team members executing different cases). Test data will be prepared using valid data and invalid data for card numbers, PIN, different deposit amounts, withdrawal amounts, transfer amounts and communication with the bank for various transactions.

All cases will be individually and thoroughly tested for diversified valid & invalid data. Results will be compared for expected outcome vs. actual outcome for all of the test cases and cases where there are issues identified will be collected & reported as defects. Detailed conditions, data utilized, SUT, priority and steps to reproduce the issues & bugs will be reported in the tracking tool.
