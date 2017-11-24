       /**  
         * Checking Account class  
         *  
         * @author Tyerra Smith and Olivia Horace  
         * @version Implementation 3.1 (09/01/2017)  
         */  
    
        public class CheckingAccount extends Account  
       {  
            // instance variables - replace the example below with your own  
             private double overdraftFee = 25.00;  
  
         /**  
           * Constructor for objects of class CheckingAccount  
           */  
  
          public CheckingAccount(String fName, String lName, String type)  
          {  
              // initialise instance variables  
              super(fName, lName, type);  
          }  
      
          public void deposit(double amount)    
          {  
             super.deposit(amount);  
          }  
      
           public void withdraw(double amount)  
           {  
               super.withdraw(amount);  
           }  
      
           public boolean transfer(Account tAccount, double amount){  
                 return super.transfer(tAccount, amount);  
              }  
       }   
