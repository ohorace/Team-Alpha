	/**  
	* Write a description of class Customer here.  
	*  
	* @Olivia Horace and Tyerra Smith  
	* @August 30, 2017  
	*/  
	public class Customer  
	{  
	private String firstName;  
	private String lastName;  
	private String social;  
	private String accountNumber;  
	private String username;  
	private String password;  

	public Customer(){  
	setFName("John");  
	setLName("Doe");  
	setSocial("123-45-6789");  
	setAccNo("C12345678");  
	setUsername("username");  
	setPassword("password");  
	}  

	public Customer(String fName, String lName, String SSN, String accountNo, String user, String pass){  
	setFName(fName);  
	setLName(lName);  
	setSocial(SSN);  
	setAccNo(accountNo);  
	setUsername(user);  
	setPassword(pass);  
	}  

	public void setFName(String fName){  
	firstName = fName;  
	}  

	public void setLName(String lName){  
	lastName = lName;  
	}  

	public void setSocial(String SSN){  
	social = SSN;  
	}  

	public void setAccNo(String accountNo){  
	accountNumber = accountNo;  
	}  

	public void setUsername(String user){  
	username = user;  
	}  

	public void setPassword(String pass){  
	password = pass;  
	}  

	public String getFName(){  
	return firstName;  
	}  

	public String getLName(){  
	return lastName;  
	}  

	public String getSocial(){  
	return social;  
	}  

	public String getAccNo(){  
	return accountNumber;  
	}  

	public String getUsername(){  
	return username;  
	}   

	public String getPassword(){  
	return password;  
	}  

	}  
