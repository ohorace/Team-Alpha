     /**  
     * Testing Class  
     * Creates 5 objects and checks their log in credentials  
     *  
     * @Horace and Smith  
     * @9/10/17 V1  
     */   
     import java.io.*;  
     import java.util.*;  
     public class Testing  
     {  
        public static void main (String args[]){  
        ArrayList<Customer> customerList = new ArrayList<Customer>();  
        Customer test1 = new Customer("Olivia", "Horace", "1", "C1", "olivia", "pass");  
        Customer test2 = new Customer("Nicole", "Horace", "2", "C2", "nicole", "pass");  
        Customer test3 = new Customer("Shannon", "Horace", "3", "C3", "shan", "pass");  
        Customer test4 = new Customer("Mary", "Horace", "4", "C4", "mary", "pass");  
        Customer test5 = new Customer("Shaquena", "Horace", "5", "C5", "shaq", "pass");   
  
        customerList.add(test1);  
        customerList.add(test2);  
        customerList.add(test3);  
        customerList.add(test4);  
        customerList.add(test5);  
  
        for(int j = 0; j <customerList.size(); j++){  
            Scanner kbReader = new Scanner(System.in);  
            System.out.print("Enter username: ");  
            String username = kbReader.nextLine();  

            System.out.print("Enter password: ");  
            String password = kbReader.nextLine();  
  
                for(int i = 0; i < customerList.size(); i++){  
                    if(customerList.get(i).getUsername().equals(username)){  
                         if(customerList.get(i).getPassword().equals(password)){  
                               System.out.println("Login successful");  
                               break;  
                         }  
                   else{  
                        System.out.println("Login unsuccessful");  
                        break;  
                   }  
             }  
               else{  
                  continue;  
               }  
           }  
     }  
     }  
     }  
