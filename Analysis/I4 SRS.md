## Team Alpha a.k.a. Tyerra Smith and Olivia Horace  
### Mobile Banking Software Requirements Specification  

#### Section 1: Requirements  

**1.1: Functional Requirements**  

* 1.1.1. The system shall allow users to login using a unique username and password.  

* 1.1.2. The username should be between 8 and 18 characters.  
-- a) Spaces are not allowed.  

* 1.1.3. The password should be between 8 and 12 characters.    
-- a) Passwords cannot contain spaces.  

* 1.1.4. The *Account Information* page (i.e. the first page displayed after logging in) shall display all of the user's accounts.  
-- a) Accounts will be sorted by account number.  

* 1.1.5. The *Account Information* page shall display the details of each account.  
-- a) Account type   
-- b) Account number  
-- c) Account balance  

* 1.1.6. The system shall allow the user to deposit cash into an account.  
-- a) The amount to be deposited will be entered.    
-- b) After a successful deposit, the account balance will be displayed.  

* 1.1.7. The system shall allow the user to transfer money from one account to another account.   
-- a) The transaction cannot be made if the **'transfer from'** account does not have insufficient funds.   
-- b) After a successful transfer, the account balances of both accounts will be displayed.   

* 1.1.8 The system shall allow the user to withdrawal money.   
-- a) The user will not be allowed to withdraw money if the account does not have sufficient funds.   
-- b) After a successful withdrawal, the account balance will be displayed.  

* 1.1.9 The system shall allow the user to get a balance query.  
-- a) The account number and the current balance of the account should be displayed.  

* 1.1.10 The system shall allow the user to print the last 3 transactions performed on the account.  
-- a) If the number of transaction performed on the account is less than 3, the transactions will still print.
-- b) If no transactions have been performed on the account, an error message will be printed to inform the user of this.
-- c) The transactions will be listed in order of recency (most recent first).
