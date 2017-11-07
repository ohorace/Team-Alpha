# Savings Account Source Code  

```java  
/**
 * Savings Account class  
 *  
 * @author Tyerra Smith and Olivia Horace  
 * @version Implementation 3.1 (09/01/2017)  
 */  
public class SavingsAccount extends Account  
{  
    private double interestRate;  
    private int maxTransactions = 6;  
    private int numOfTransactions;  
  
    /**  
     * Constructor for objects of class SavingsAccount  
     */  
    public SavingsAccount(String fName, String lName, String type, double interestRate)  
    {  
        super(fName, lName, type);  
        this.interestRate = interestRate;  
        this.numOfTransactions = 0;  
    }  
  
    /**  
     * This method will be used to calculate the interest accumulated.  
     *  
     *  
     * @return    the product of interestRate and accountBal  
     */  
    public double calculateInterest()  
    {  
        return interestRate * accountBal;  
    }  
  
    public int getNumOfTransctions(){  
        return numOfTransactions;  
    }  
}
```
