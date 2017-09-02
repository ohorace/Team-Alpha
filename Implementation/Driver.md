	/**  
	* Driver class  
	*  
	* @Horace and Smith 
	* @August 31, 2017
	*/  

	import java.io.*;  
	import java.util.*;  
	public class Driver  
	{  
		public static void main (String args[]){  
		System.out.println("Welcome to online banking");  

		ArrayList<Customer> customerList = new ArrayList<Customer>();  
		Customer test = new Customer();  

		customerList.add(test);  

		Scanner kbReader = new Scanner(System.in);  
		System.out.print("Enter username: ");  
		String username = kbReader.nextLine();  

		System.out.print("Enter password: ");  
		String password = kbReader.nextLine();

		for(int i = 0; i < customerList.size(); i++){  
			if(customerList.get(i).getUsername().equals(username)){  
				if(customerList.get(i).getPassword().equals(password)){  
					System.out.println("Login sucessful");  
					break;  
				}  
				else{  
					System.out.println("Login unsucessful");  
					break;  
				}  
			}  
			
			else{  
				System.out.println("Login unsucessful");  
				break;  
			}  
		}  
	    }  
	}  
