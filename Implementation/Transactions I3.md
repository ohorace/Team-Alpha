# Transactions Source Code  

```java
public class Transactions
{
    // instance variables - replace the example below with your own
    private int x;

    /**
     * Constructor for objects of class Transaction
     */
    public Transactions()
    {
        // initialise instance variables
        x = 0;
    }

    public String withdraw(Account account, double amount)
    {
        double balance = account.getAccountBal();
        if (balance < amount){
            return "Your withdrawal was unsuccessful because you have insufficient funds. Your account balance for account number " + 
            account.accountNo + " is $" + balance + ".";
        }
        
        else{
            account.accountBal -= amount;
            return "Your withdrawal was successful. Your new account balance for account number " + account.accountNo + " is $" 
            + account.accountBal + ".";
        }   
        
        //TODO: We have to figure out how we will handle overdrafting.
    }
    
    public String deposit(Account account, double amount)
    {
        account.accountBal += amount;
        return "Your deposit was successful. Your new account balance for account number " + account.accountNo + " is $" + 
        account.accountBal + ".";
    }
    
    public String transfer(Account sourceAccount, Account destinationAccount, double amount)
    {
        double sourceBalance = sourceAccount.getAccountBal();
        if (sourceBalance < amount){
            return "Your transfer was unsuccessful because you have insufficient funds. Youraccount balance for account number " + 
            sourceAccount.accountNo + " is $" + sourceBalance + ".";
        }
        //TODO: If the source account is a savings account, we should check if the maximum number of transactions have been reached.
        
        else{
            sourceAccount.accountBal -= amount;
            destinationAccount.accountBal += amount;
            return "Your transfer was successful because you have insufficient funds. Your new account balance for account number " + 
            sourceAccount.accountNo + " is $" + sourceAccount.accountBal + ". Your new account balance for account number " + 
            destinationAccount.accountNo + " is $" + destinationAccount.accountBal + ".";
        }
    }
}
```
