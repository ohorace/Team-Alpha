```java

/**
 * Customer Class used for logins
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

    /**
     * Default Customer Constructor
     */
    public Customer(){
        setFName("John");
        setLName("Doe");
        setSocial("123-45-6789");
        setAccNo("C12345678");
        setUsername("username");
        setPassword("password");
    }

    /**
     * Custom Customer constructor
     * @param fName, lName, SSN, accountNo, user, pass
     */
    public Customer(String fName, String lName, String SSN, String accountNo, String user, String pass){
        setFName(fName);
        setLName(lName);
        setSocial(SSN);
        setAccNo(accountNo);
        setUsername(user);
        setPassword(pass);
    }
    
    /**
     * Custom constructor that only accepts name and log in info
     * @param fName, lName, user, pass
     */
    public Customer(String fName, String lName, String user, String pass){
        setFName(fName);
        setLName(lName);
        setUsername(user);
        setPassword(pass);
        
    }

    /**
     * Set first name method
     * @param fName
     */
    public void setFName(String fName){
        firstName = fName;
    }

    /**
     * Set last name method
     * *param lName
     */
    public void setLName(String lName){
        lastName = lName;
    }

    /**
     * Set social security method
     * @param SSN
     */
    public void setSocial(String SSN){
        social = SSN;
    }

    /**
     * Set account number method
     * @param accountNo
     */
    public void setAccNo(String accountNo){
        accountNumber = accountNo;
    }

    /**
     * Set username method
     * @param user
     */
    public void setUsername(String user){
        username = user;
    }

    /**
     * Set password method
     * @param pass
     */
    public void setPassword(String pass){
        password = pass;
    }

    /**
     * Get first name method
     * @return firstName
     */
    public String getFName(){
        return firstName;
    }

    /**
     * Get last name method
     * @return lastName
     * 
     */
    public String getLName(){
        return lastName;
    }

    /**
     * Get social method
     * @return social
     */
    public String getSocial(){
        return social;
    }

    /**
     * Get account number method
     * @return accountNumber
     */
    public String getAccNo(){
        return accountNumber;
    }

    /**
     * Get username method
     * @return username;
     */
    public String getUsername(){
        return username;
    }

    /**
     * Get password method
     * @return password
     */
    public String getPassword(){
        return password;
    }

}
```
