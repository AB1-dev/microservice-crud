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

Mysql queries:
-------------

5) Create a Database in Mysql command line(Banking)

5) Import Create query in the Mysql

7)Insert data using Bank.sql file 

8) Create a connection to DB by giving necessary details in application.properties

STS coding:
-----------
9)Create an Entity class with variables and getter and setter methods for those (Bank.java)

10)create a DAO interface and add methods which perform CRUD operations(BankDAOImpl.java)

11) Implement those methods in DAO class.(BankDAO.java)

12) Create a service with abstract methods to call methods in DAO.(BankServiceImpl.java)

13)Create a service class to implement the service interface (BankService.java)

14)Now at last create Restcontroller class using @RestController (BankDetailsController.java)



Testing:
--------
15) Run the BankDetailsApplication.java class

16) Now using postman test the CRUD operations.

GET (All details):  http://localhost:8080/BankService/bank

POST: http://localhost:8080/BankService/bank

Body:{"amount": 50436,
    "address2": "moscow",
    "phone": "9867622",
    "email": "kirra@gmail.com",
    "accountNumber": 1238719877,
    "lastName": "Joe",
    "address1": "japan",
    "firstName": "kiran"
}

PUT:  http://localhost:8080/BankService/bank/1238719874

Body:{"amount": 50000,
    "address2": "Karnataka",
    "phone": "9867622",
    "email": "Blessin@gmail.com",
    "accountNumber": 1238719875,
    "lastName": "Joe",
    "address1": "Banglore",
    "firstName": "Blessin"
}

DELETE: http://localhost:8080/BankService/bank/1238719877

PATCH: http://localhost:8080/BankService/bank/1238719874

Body:{"amount": 10000001,
    "address2": "Telangana",
    "phone": "9642589",
    "email": "abc@gmail.com",
    "accountNumber": 1238719874,
    "lastName": "qwerty",
    "address1": "Hyderabad",
    "firstName": "Bharath"}
    
GET (By AccountNumber):  http://localhost:8080/bank/1238719873



