**Exploratory (Manual Non-scripted) Testing Plan ATM SUT V1.0**

**Test Plan:**

The test plan for Manual Non Scripted testing will prioritize all key operations & functions of the ATM SUT V1.0. The key areas, functions & operations that the Manual Non Scripted testing will be following as listed below, which are expected to be used by either users & operators:

1. ATM Operator Panel Functions And Logging
2. Card PIN validation and PIN verification
3. Transactions:
  1. Cash withdrawal
  2. Deposit processing
  3. Money transfer
  4. Balance inquiry
4. Transaction cancellation
5. Communication with the bank
6. Receipt Generation & Display
7. User interface
8. Operator functions (start/stop, cash verification, log entries)
9. Access to shared accounts & transactions

The key components for the testing environment will be following as listed below:

1. ATM Simulation V1.0 is the SUT
2. Available cards & PINs:
  1. Card 1, PIN 42
  2. Card 2, PIN 1234
3. Initial Holding Balance of Cards
  1. Card 1
    1. Chequing (Shared): $100
    2. Savings: $1000
  2. Card 2
    1. Chequing (Shared): $100
    2. Savings: $1000
    3. Money Market: $5000
4. Diversified testing data:
  1. Various amounts of withdrawal, deposit, transfer amounts
  2. Balance inquiries on different accounts
5. Banking communication & system networking

**Testing Strategy & Cases:**

For each of the key operations, functions and areas for SUT defined above, the following strategy is defined for the Manual Non Scripted testing. Common paths and exceptional paths are defined within the cases.

**Operator Panel:**

1. Test on/off operation of ATM and logging (common)

**Card Validation:**

1. Test available Card (1 and 2) (common)
2. Test invalid Cards
3. Test invalid PINs
4. Test valid Cards with Invalid PINs and valid PINs after unsuccessful PINs

**Transactions:**

1. _Deposits:_
  1. Test various amount for deposits (common)
  2. Test deposits in multiple accounts (common)
  3. Confirm receipt & log details with deposits (common)
2. _Withdrawals:_
  1. Test different amounts for withdrawals (common)
  2. Test withdrawals in all accounts (common)
  3. Confirm with receipt and SUT log (common)
  4. Withdraw invalid amounts exceeding balance (exceptional)
3. _Transfer:_
  1. Test transferring between different accounts and ensure all account have transferred from and to (common)
  2. Transfer invalid or insufficient amounts (exceptional)
  3. Transfer to invalid accounts (exceptional)
4. _Balance Inquiry_
  1. Test balance reporting of all valid accounts (common)
  2. Test balance reporting of invalid accounts (exceptional)
  3. Confirm receipt and log verification with balance inquiries (common)
5. _Transaction Operations:_
  1. Confirm transaction cancel, continue and ejection operations for different stages (common)
6. _User Interface:_
  1. Test all operations and buttons on the user interface for different SUT pages (exceptional)
  2. Test output of different operations in the display and receipts (exceptional)
7. _Receipts:_
  1. Confirm receipt data is validated with system log (exceptional)
  2. Confirm receipt displays correct information for the transactions (common)

**Testing Execution & Reposting of Issues:**

To execute testing of the testing cases, each of the above test cases will be followed (with different team members executing different cases). Test data will be prepared using valid data and invalid data for card numbers, PIN, different deposit amounts, withdrawal amounts, transfer amounts and communication with the bank for various transactions.

All cases will be individually and thoroughly tested for diversified valid & invalid data. Results will be compared for expected outcome vs. actual outcome for all of the test cases and cases where there are issues identified will be collected & reported as defects. Detailed conditions, data utilized, SUT, priority and steps to reproduce the issues & bugs will be reported in the tracking tool.
