```java
/**
 * Testing Class
 * Creates 5 Account objects
 * 
 * 
 * @Horace and Smith 
 * @October 16, 2017 - Iteration 2
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

        while(true){
        try{
            for(int j = 0; j < accountList.size(); j++){
                Scanner kbReader = new Scanner(System.in);
                System.out.print("Enter deposit amount: ");
                double deposit = Double.parseDouble(kbReader.nextLine());
                if(deposit >= 0){
                    accountList.get(j).deposit(deposit);
                    System.out.printf("Transaction successful!" + "\nAccount Balance: $%.2f\n", accountList.get(j).getAccountBal());
                }
                else{
                    System.out.println("Error: Please only enter non-negative dollar amount!");
                    continue;
                }

                System.out.print("Enter withdrawl amount: ");
                double withdraw = Double.parseDouble(kbReader.nextLine());

                if(withdraw >= 0){
                    accountList.get(j).withdraw(withdraw);
                    System.out.printf("Transaction successful!" + "\nAccount Balance: $%.2f\n", accountList.get(j).getAccountBal());
                }
                else{
                    System.out.println("Error: Please only enter non-negative dollar amount!");
                    continue;
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
