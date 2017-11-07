# Account Source Code
'''java  

/**
 * Account class
 *
 * @author Tyerra Smith and Olivia Horace
 * @version Implementation 3.1 (09/01/2017)
 */

import java.util.Random;
public class Account
{
    // instance variables  
    protected String accountType;  
    protected String accountNo;  
    protected double accountBal;  
    protected String accountOwnerFName;  
    protected String accountOwnerLName;  
    //private double accountStartupAmt; If a new account is being created, for a Savings account you must start with at least $25  
    
    /**
     * Constructor for objects of class Account
     */
    public Account(String fName, String lName, String type)
    {
        // initialise instance variables
        accountOwnerFName = fName;
        accountOwnerLName = lName;
        accountType = type;
        accountBal = 0.00;
        accountNo = generateAccountNo();
    }


    public void setType(String type)
    {
        accountType = type;
    }
    
    public void setOwnerFname(String fName)
    {
        accountOwnerFName = fName;
    }
    
    public void setOwnerLname(String lName)
    {
        accountOwnerLName = lName;
    }
    
    public String generateAccountNo()
    {
        String accountNo;
        int randNum;
        if (accountType == "checking")
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
    
    public String getAccountOwner()
    {
        return accountOwnerFName + " " + accountOwnerLName;
    }
    
    public String getAccountNo()
    {
        return accountNo;
    }
    
    public double getAccountBal()
    {
        return accountBal;
    }
    
    public String getAccountType()
    {
        return accountType;
    }
    
}