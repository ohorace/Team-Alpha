## Team Alpha a.k.a. Tyerra Smith and Olivia Horace  
### Mobile Banking Software Requirements Specification  

#### Section 1: Requirements  

**1.1: Functional Requirements**  

* 1.1.1. The system shall allow users to login using a unique username and password.  
-- a) Maximum of 3 failed attempts before the account is locked.  

* 1.1.2. The username should be between 8 and 18 characters.  
-- a) The username can only contain alphanumeric characters.  
-- b) Symbols and spaces are not allowed.  

* 1.1.3. The password should be between 8 and 12 characters.
-- a) The password must contain *at least*: one capital letter, one lowercase letter, one number, and one special character.  
-- b) Passwords cannot contain spaces.  

* 1.1.4. The *Account Information* page (i.e. the first page displayed after logging in) shall display all of the user's accounts.  
-- a) Accounts will be sorted by account number.  

* 1.1.5. The *Account Information* page shall display the details of each account.  
-- a) Account type   
-- b) Account number  
-- c) Account balance  
-- d) Last 3 transactions  

* 1.1.6. The system shall allow the user to deposit cash into an account.
-- a) The amount to be deposited will be entered. 
-- b) If the transaction limit has been reached, the deposit will not be completed.    
-- c) After a successful deposit, the account balance will be displayed. 

* 1.1.7. The system shall allow the user to transfer money from one account to another account.  
-- a) The transaction cannot be made if the **transfer from** account does not have insufficient funds. 
-- b) If the transaction limit has been reached, the transfer will not be completed.  
-- c) After a successful transfer, the account balances of both accounts will be displayed.   

* 1.1.8 The system shall allow the user to withdrawl money.  
-- a) The user will not be allowed to withdraw money if the account does not have sufficient funds.  
-- b) If the transaction limit has been reached, the deposit will not be completed. 
-- c) After a successful withdrawl, the account balance will be displayed.  
