```java
/**
 * Testing Class
 * Creates 5 Account objects
 * 
 * 
 * @Horace and Smith 
 * @November 25, 2017 - Iteration 3
 */
import java.io.*;
import java.util.*;
public class TestingI3
{
    public static void main (String args[]){
        ArrayList<Account> accountList = new ArrayList<Account>();

        accountList.add(new Account("Olivia", "Horace", "Checking"));
        accountList.add(new Account("Tyerra", "Smith", "Saving"));
        accountList.add(new Account("Mike", "Pickard", "Checking"));
        accountList.add(new Account("Darian", "Thomas", "Saving"));
        accountList.add(new Account("Cam", "Baker", "Checking"));

        Transactions newTran = new Transactions();
        while(true){
            try{
				/////////////////////////////////////////////////////////////////
				/////////////////////Positive Testing////////////////////////////
				////////////////////////////////////////////////////////////////
				System.out.println("***Positive Testing***");
                //deposits
                for(int j = 0; j < accountList.size(); j++){
                    System.out.println(newTran.deposit(accountList.get(j), 100));
                }

                //withdrawals
                for(int j = 0; j < accountList.size(); j++){
                    System.out.println(newTran.withdraw(accountList.get(j), 5));
                }

                //transfer
                for(int j = 0; j < accountList.size(); j++){
                    if (j == accountList.size() - 1){
                        System.out.println(newTran.transfer(accountList.get(j), accountList.get(0), 20));
                    }
                    else{
                        System.out.println(newTran.transfer(accountList.get(j), accountList.get(j+1), 20));
                    }
                }

				/////////////////////////////////////////////////////////////////
				/////////////////////Negative Testing////////////////////////////
				////////////////////////////////////////////////////////////////
				System.out.println("***Negative Testing***");
                //deposits
                for(int j = 0; j < accountList.size(); j++){
                    System.out.println(newTran.deposit(accountList.get(j), -20));
                }

                //withdrawals
                for(int j = 0; j < accountList.size(); j++){
                    System.out.println(newTran.withdraw(accountList.get(j), 500));
                }

                //transfer
                for(int j = 0; j < accountList.size(); j++){
                    if (j == accountList.size() - 1){
                        System.out.println(newTran.transfer(accountList.get(j), accountList.get(0), 200));
                    }
                    else{
                        System.out.println(newTran.transfer(accountList.get(j), accountList.get(j+1), 201));
                    }
                }
                break;
            }
            catch(Exception e)
            {
                System.out.println("Error: Please only enter non-negative dollar amount!");
            }
        }
    }
}
```