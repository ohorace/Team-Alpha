```java
/**
 * Account class
 *
 * @author Tyerra Smith and Olivia Horace
 * @version Implementation 3.1 (09/01/2017)
 */

//import java.util.Random;
import java.util.*;
import java.text.DecimalFormat;
public class Account
{
    // instance variables 
    protected String accountType;
    protected String accountNo;
    protected double accountBal;
    protected String accountOwnerFName;
    protected String accountOwnerLName;
    DecimalFormat df = new DecimalFormat("0.00");
    protected static ArrayList<Transactions> transactionsList; 
    //private double accountStartupAmt; If a new account is being created, for a Savings account you must start with at least $25
    
    /**
     * Constructor for objects of class Account
     */
    public Account(String fName, String lName, String type)
    {
        // initialise instance variables
        setOwnerFname(fName);
        setOwnerLname(lName);
        setType(type);
        accountBal = 0.00;
        accountNo = generateAccountNo();
        setTransList();
    }


    /**
     * Set Type method
     * Sets account type; either checking or savings
     * @param type
     */
    public void setType(String type)
    {
        accountType = type;
    }
    
    /**
     * Set account owner first name
     * @param fName
     */
    public void setOwnerFname(String fName)
    {
        accountOwnerFName = fName;
    }
    
    /**
     * Set account owner last name
     * @param lName
     */
    public void setOwnerLname(String lName)
    {
        accountOwnerLName = lName;
    }
    
    /**
     * Set transaction list
     * Creates an array list of transactions
     */
    public void setTransList()
    {
        transactionsList = new ArrayList<Transactions>(); 
    }
    
    /**
     * Generate account number method
     * @return accountNo
     */
    public String generateAccountNo()
    {
        String accountNo;
        int randNum;
        if (accountType.equalsIgnoreCase("checking"))
        {
            accountNo = "C";
        }
        else //accountType == "savings"
        {
            accountNo = "S";
        }
        
        //Check to see if this works for generating a random 9-digit account number
        randNum = 100000000 + (new Random().nextInt(900000000));
        accountNo += Integer.toString(randNum);
        
        return accountNo;
    }
    
    /**
     * Get account owner 
     * @return account owner first and last name
     */
    public String getAccountOwner()
    {
        return accountOwnerFName + " " + accountOwnerLName;
    }
    
    /**
     * Get account number method
     * @return accountNo
     */
    public String getAccountNo()
    {
        return accountNo;
    }
    
    /**
     * Get account balance method
     * @return accountBal
     */
    public double getAccountBal()
    {
        return accountBal;
    }
    
    /**
     * Get account type method
     * @return accountType
     */
    public String getAccountType()
    {
        return accountType;
    }
    
    /**
     * To string method
     * @return string of account information
     */
    public String toString()
    {
        return "\nAccount Information\n" + accountOwnerFName + " " + accountOwnerLName + "\nAccount Number: " + accountNo +
        "\nAccount Type: " + accountType + "\nAccount Balance: $" + df.format(accountBal);
    }
    
}
```
