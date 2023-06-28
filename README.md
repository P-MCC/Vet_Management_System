# Veterinary Management System
Simple veterinary management system build using JavaFX


### How to run? 
Before running the program.

First of all you have to modify the Connect.java class which is placed in src/main/java/JDBC/Connect.java
in this class database connection properties are given. Change those properties to fit your database.(Like your localhost password and port number(THIS IS IMPORTANT!)

Implement the database by using VMSDBSQL.SQL file it is placed in `src/main/vmsDB/VMSDBSQL.SQL`
or you can simply add our updated veterinary_management_system(final).sql file (from Phase2) to XAMPP , MySQL Workbench etc..

You don’t need to add vm options or external libraries. JavaFX and MYSQL Connector/J is implemented 
via Maven, in the indexing phase those libraries will be downloaded automatically.


 3 different ways to run the project

1. By opening the V_M_S_F file in an IDE (IntelliJ or Eclipse) basically press the run button.
![](assets/way-1.png)


2. In IntelliJ at the right there is a tab called Maven by opening it you will reveal 3 packages. 
 n the Plugins then the javafx package after that double click the `javafx:run`
![](assets/way-2.png)

   
3. By using CMD (Terminal) go into the path of V_M_S_F package and run the following command
  ```mvn clean install package javafx:run``` 
![](assets/way-3.png)


### Database Design 
![](assets/db.png)


### IMPORTANT NOTE on INSERT/UPDATE/DELETE OPERATIONS:

If you want an efficient database app, you should make an "insert" operation considering the following order.

customer -> customerphonenumber -> PetCharacteristic -> Pet ->  Service -> Invoice -> Needs -> Vet -> Provides

-Also, you cannot update IDs in all tables because these IDs are unique.(Only insert and delete)


