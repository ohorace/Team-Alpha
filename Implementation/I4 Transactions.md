```java
import java.util.*;
import java.text.DecimalFormat;
/**
 * Class for Transactions 
 *
 * @Tyerra Smith and Olivia Horace
 * @V3
 */
public class Transactions
{
    DecimalFormat df = new DecimalFormat("0.00");
    String transactionInfo = null;
    /**
     * Generate Transaction Number method
     * Creates a random transaction number
     * @return transNo
     */
    public static int generateTransNumber(){
        Random rn = new Random();
        int transNo = 100000 + rn.nextInt(900000);
        return transNo;
    }

    /**
     * Withdraw method
     * @param account, amount
     * @return true if successful, false if otherwise
     */
    public boolean withdraw(Account account, double amount)
    {
        boolean successful = false;
        if(amount < 0){
            System.out.println("\nYour withdrawal was unsuccessful");
        }
        else{
            double balanceOld = account.getAccountBal();

            if (balanceOld < amount){
                System.out.println("\nYour withdrawal was unsuccessful because you have insufficient funds. \nYour account balance for account number " + 
                account.accountNo + " is $" + df.format(balanceOld) + ".\n");
            }

            else{
                account.accountBal -= amount;
                int transNumber = generateTransNumber();
                
                System.out.println("Your withdrawal was successful.");
                
                transactionInfo = "\nTransaction Number: " + transNumber + "\nWITHDRAWAL from Account: " + account.accountNo + "\n Amount: $." + amount
                + "\nSTARTING balance: $" + df.format(balanceOld) + "\nENDING balance: $" + df.format(account.accountBal) + "\n";
                successful = true; 
            } 
        }  
        return successful;
        //TODO: We have to figure out how we will handle overdrafting.
    }

    /**
     * Deposit method
     * @param account and amount
     * @return true if successful, false if otherwise
     */
    public boolean deposit(Account account, double amount)
    {
        boolean successful = false;
        if(amount < 0){
            System.out.println("\nYour deposit was unsuccessful");
        }
        else{
            double balanceOld = account.accountBal;
            int transNumber = generateTransNumber();
            account.accountBal += amount;
            System.out.println("\nYour deposit was successful.");
            
            transactionInfo = "\nTransaction Number: " + transNumber + "\nDEPOSIT to Account: " + account.accountNo + "\n Amount: $." + amount
             + "\nSTARTING balance: $" + df.format(balanceOld) + "\nENDING balance: $" + df.format(account.accountBal) + "\n";
            successful = true;
        }   
        return successful;
    }

    /**
     * Transfer method
     * @param sourceAccount, destinationAccount, amount
     * @return true if successful, false if otherwise
     */
    public boolean transfer(Account sourceAccount, Account destinationAccount, double amount)
    {
        boolean successful = false;
        if(amount < 0){
            System.out.println("\nYour transfer was unsuccessful");
        }
        else{
            double sourceBalanceOld = sourceAccount.getAccountBal();
            if (sourceBalanceOld < amount){
                System.out.println("\nYour transfer was unsuccessful because you have insufficient funds. \nYour account balance for account number " + 
                sourceAccount.accountNo + " is $" + df.format(sourceBalanceOld) + ".\n");
            }
            //TODO: If the source account is a savings account, we should check if the maximum number of transactions have been reached.

            else{
                int transNumber = generateTransNumber();
                double destinationBalanceOld = destinationAccount.accountBal;
                sourceAccount.accountBal -= amount;
                destinationAccount.accountBal += amount;
                System.out.println("\nYour transfer was successful."); 
                transactionInfo = "\nTransaction Number: " + transNumber + "\nTRANSFER FROM Account: " + sourceAccount.accountNo + 
                "\nTRANSFER TO Account: " + destinationAccount.accountNo + "\n Amount: $." + amount + "\nSOURCE Account STARTING balance: $" 
                + df.format(sourceBalanceOld) + "\nSOURCE Account ENDING balance: $" + df.format(sourceAccount.accountBal) + 
                "\nDESTINATION Account STARTING balance: $" + df.format(destinationBalanceOld) + "\nDESTINATION ACCOUNT ENDING balance: $" + 
                df.format(destinationAccount.accountBal) + "\n";
                successful = true;
            }
        }
        return successful;
    }
}
```
