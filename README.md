# Web-Customer-Tracker
A customer relationship management app which leverages Spring MVC, Hibernate and MySQL database to display a list of customers and apply CRUD operations. Spring Security has been utilized to prevent access to the customer list page and also specific functionalities of the app based on roles. Moreover, user registration has also been implemented in which validation is performed to existing users. Also, bcrypt encryption for passwords is implemented for storing in the database. Lastly, Spring AOP has been implemented for logging. 

More details below.

![Screenshot](https://github.com/RaviShankarKondoju/Web-Customer-Tracker/blob/master/customer-crudd-app-with-security-jdbc-encryption-authentication/src/main/webapp/resources/images/manager-access.PNG)'

# Technology
- Front End
  - HTML
  - CSS
  - JavaScript
  - Bootstrap
 
 - Back End
    - Java
    - Spring MVC
    - Spring Security
    - Spring AOP
    - Hibernate
  
 - Database
    - MySQL
    
 - Server
    - Apache Tomcat
    
 
 - Platform
    - Windows 10
    
# Features

- Security
  - Signup Page
    - users need to sign up to gain access to the customer list page. Here, validation is performed by checking if a user already exists in the database. Also, passwords are stored in bycrypt format for security. 
    ![user-registration-form](https://user-images.githubusercontent.com/33348004/53510723-a6fc0700-3ae4-11e9-8206-fff0aabf2e26.PNG)
  - Validation
    - Username and password cannot be empty
  ![user-registration-form-validation](https://user-images.githubusercontent.com/33348004/53510897-0c4ff800-3ae5-11e9-8689-13cedf54adac.PNG)

  -   login page
    - Only users with valid id/passwords will be able to login.
    ![login-page](https://user-images.githubusercontent.com/33348004/53510165-59cb6580-3ae3-11e9-831b-f1d5330c5fcc.PNG)
    - Validation
    ![login-page-validation](https://user-images.githubusercontent.com/33348004/53510224-74054380-3ae3-11e9-81e5-e162f28cfa04.PNG)
    - The app also resrticts access based on roles
      - Employee role: users in this role will only be allowed to list and search customers.
      ![employee-access](https://user-images.githubusercontent.com/33348004/53510539-3ead2580-3ae4-11e9-9b0a-38667815cfba.PNG)
      - Manager role: users in this role will be allowed to list, add, update and search customers.
      ![manager-access](https://user-images.githubusercontent.com/33348004/53510565-4ff63200-3ae4-11e9-994d-1932ba733725.PNG)
      - Admin role: users in this role will be allowed to list, add, update, delete and search customers.
      ![admin-access](https://user-images.githubusercontent.com/33348004/53510576-597f9a00-3ae4-11e9-9c3c-f2272d5c5f40.PNG)

- Adding customers
  - a form is presented in which the user can enter a first name, last name and email as well as go back to the list page.
  
  ![customer-form](https://user-images.githubusercontent.com/33348004/53490867-ced67500-3aba-11e9-9dfc-dea6ce9975e1.PNG)
 
- updating customers
  - When a user selects an update for a particular customer, the specific user id is passed to the URL from which the details of a customer are fetched and populated in the form.
  - The user can make necessary updates and click save.
 
  ![update-page](https://user-images.githubusercontent.com/33348004/53490970-1ceb7880-3abb-11e9-84c2-a6bd9e77701d.PNG)

- deleting customers
  - When a user selects delete, a prompt appears to confirm his action.
  - If yes, a specific user is deleted.
  - If no, the action is cancelled.
 
  ![delete-info](https://user-images.githubusercontent.com/33348004/53491260-f974fd80-3abb-11e9-90a3-3ad0ac19b761.PNG)

- Search functionality
  - A search box has been added which allows a user to search by name
  - On the backend, the input name will be compared to the customer's first name or last name in the database. 
  - If the input is empty, the entire customer list is returned.
  - If the input is not empty, we can search for substrings.

- Spring AOP for logging
  - @Before advice has been used to display the calling method and the arguments in the logger before method call.
  - @AfterReturning advice has been implemented to display the calling method and the results in the logger after a method call.
  - Pointcut expressions have been utilized to implement the advice on every method.
