# microservice-crud

This micro service is to create a REST Api using springboot to support CRUD operations.

Prerequisites:
--------------
1) Install JDK, JRE and maven installed in your machine

2)Install Spring Tool Suite(STS)
link: https://spring.io/tools

3)Install Mysql 
link: https://www.mysql.com/downloads/

4)Install PostMan
link: https://www.getpostman.com/downloads/

5)Install gitbash
link: https://git-scm.com/downloads

Mysql queries:
-------------

5) Create a Database in Mysql command line(Banking)

5) Import Create query in the Mysql

7)Insert data using Bank.sql file 

8) Create a connection to DB by giving necessary details in application.properties

![databse initial records](https://user-images.githubusercontent.com/57008406/67829957-f32d9a00-fafe-11e9-85d2-6585fb8e5504.PNG)

STS coding:
-----------
9)Create an Entity class with variables and getter and setter methods for those (Bank.java)

10)create a DAO interface and add methods which perform CRUD operations(BankDAOImpl.java)

11) Implement those methods in DAO class.(BankDAO.java)

12) Create a service with abstract methods to call methods in DAO.(BankServiceImpl.java)

13)Create a service class to implement the service interface (BankService.java)

14)Now at last create Restcontroller class using @RestController (BankDetailsController.java)

Code Check in:
--------------
1) Use gitbash to check in the code to remote branch

![git bash to checkin code](https://user-images.githubusercontent.com/57008406/67830057-5a4b4e80-faff-11e9-83fe-d06529fcae7e.PNG)


Testing:
--------
15) Run the BankDetailsApplication.java class

16) Now using postman test the CRUD operations.

##GET (All details):  http://localhost:8080/BankService/bank

![get request to retrieve all the records](https://user-images.githubusercontent.com/57008406/67830055-5a4b4e80-faff-11e9-9be5-4a151c946e44.PNG)

##POST: http://localhost:8080/BankService/bank

Body:{"amount": 50436,
    "address2": "moscow",
    "phone": "9867622",
    "email": "kirra@gmail.com",
    "accountNumber": 1238719877,
    "lastName": "Joe",
    "address1": "japan",
    "firstName": "kiran"
}
##Post response:
--------------

![post response](https://user-images.githubusercontent.com/57008406/67830063-5ae3e500-faff-11e9-95ad-55638f2f69e6.PNG)


##PUT:  http://localhost:8080/BankService/bank/1238719874

Body:{"amount": 50000,
    "address2": "Karnataka",
    "phone": "9867622",
    "email": "Blessin@gmail.com",
    "accountNumber": 1238719875,
    "lastName": "Joe",
    "address1": "Banglore",
    "firstName": "Blessin"
}

##put Request:

![put request](https://user-images.githubusercontent.com/57008406/67830064-5b7c7b80-faff-11e9-8560-94c25ffdcadf.PNG)

##put response:
![put response](https://user-images.githubusercontent.com/57008406/67830065-5b7c7b80-faff-11e9-9a03-d0e638979f93.PNG)

![DB after put request](https://user-images.githubusercontent.com/57008406/67830051-59b2b800-faff-11e9-8fc1-4a9eb794df08.PNG)

##DELETE: http://localhost:8080/BankService/bank/1238719877

![delete request](https://user-images.githubusercontent.com/57008406/67830053-59b2b800-faff-11e9-9e29-f545b02f0904.PNG)

##PATCH: http://localhost:8080/BankService/bank/1238719874

Body:{"amount": 10000001,
    "address2": "Telangana",
    "phone": "9642589",
    "email": "abc@gmail.com",
    "accountNumber": 1238719874,
    "lastName": "qwerty",
    "address1": "Hyderabad",
    "firstName": "Bharath"}
    
 ![Patch request](https://user-images.githubusercontent.com/57008406/67830061-5ae3e500-faff-11e9-8e4e-bb1cff4ddc1a.PNG)
    
##GET (By AccountNumber):  http://localhost:8080/bank/1238719873

![get request for a particular id](https://user-images.githubusercontent.com/57008406/67830054-5a4b4e80-faff-11e9-93bc-1210b08cbf7b.PNG)



