
     /**
      * Savings Account class
      *
      * @author Tyerra Smith and Olivia Horace
      * @version Implementation 3.1 (09/01/2017)
      */
       
      public class SavingsAccount extends Account
      {
        // instance variables - replace the example below with your own
        private double interestRate;
        private int maxTransactions = 6;

        /**
         * Constructor for objects of class SavingsAccount
         */
        public SavingsAccount(String fName, String lName, String type, double interestRate)
        {
         super(fName, lName, type);
         this.interestRate = interestRate;
        }

       /**
        * This method will be used to calculate the interest accumulated.
        *
        * 
        * @return    the product of interestRate and accountBal
        */
       public double calculateInterest()
       {
          // put your code here
          return interestRate * accountBal;
       }
    }
