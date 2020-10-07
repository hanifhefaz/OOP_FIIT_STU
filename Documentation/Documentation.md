## Library Management System in OOP

According to my Zamer, declared in the beginnig of the semester, I have tried to implement all the feutures, as mentioned there. 
I also tried to implement database for saving the data.

So far the applicaiton is capable of doing the basic operation for a library. Different users can login, such as Librarian, Clerk and borrower and do thier related jobs there.
After a successful login the user will be able to see his/her related part of the application.

I also fucosed on the main criteria of the project and tried to implement the concepts of object-oriented mechanisms in the program (appropriate use of inheritance, encapsulation, and aggregation).

Below is the class diagram for the application.

![Image](https://github.com/OOP-FIIT/oop-2019-uto-18-c-sulaimankhail-hanifhefaz/blob/master/Documentation/classes.PNG)

#### Structure of the classes

**Book**

This class is used for the properties of the books, like id, name, author, subject and if its on hold by someone for a reservation. some getters and setters are also implemented in this class. also it processes hold requestes by `processHoldRequestForBook` method. and place a book on hold by `placeThisBookOnHold` method. its also responsible for checkin and checkout.

**Person**

This is an abstract class, and holds the properties of a person, namely, id, name, address, phone and password.

**Borrower**

This class inherites `Person` class, and also process hold request for a specific borrower and amount of the books he borrowed.

**Members**

This class also inherites `Person` class and also is responsible for member's salary.

**Librarian**

This class inherites `Members` class.

**Loan**

This class is responsible for issuing and returning books. it processes the information related to an issuance or a return of a book such as who issued the book, who returned it and the date for this. it also process the extension of an issuance.

**Library**

Holds persons, books, Librarians and loans. also process some basic functionality of the system sucha as search, and adding. this class also processes database queries, which populates data from database.

## System's Structure

after a successful login a user can see all the books and place a request for reservation. if there is already a request for that book, then, he/she will not be able to do so. a librarian is capable of doing most of the functionalities of the application, such as adding book, editing book, reservation, personal info, check out, check in, adding a borrower, deleting books and others.

a clerk will be able to do some of the functionalities of the system like check in , check out, renew book, add borrower, update information and others.

The application is using mysql database. most of the code is commented out to clarify what it does.
