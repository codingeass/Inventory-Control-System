Inventory Control System
========================

Software in Java to control the buying and Selling of inventories.Helps in interaction between producer and consumer

The Prgramming Language used is **Java** .

For handling data it uses **MySQL** database.

### About this system ###
An Inventory Control System is an integrated package of software and hardware used in warehouse operation, and elsewhere, to monitor the quantity, location and status of inventory as well as the related shipping, receiving, picking and put away process. In common usage, the term may also refer to just the software components. The system will keep a log of the spares available and also be intelligent enough which spares have been taken from which supplier and in which quantity plus the amount of spares being sold to individual customer under what requirement. It will also indicate how many spares will be available for individual sectors and what should be the buying price so that we have a selling profit . Inventory Control System also include system to sell products and create bill. It include java source code, ODBC, MySQL . 

Front End of this Application look like this

![TDD](http://i.imgur.com/o7TbB6u.png?1)

## MySQL database 

Name of the database used is **practise** .
### Tables used by this System  ###

    Item 1
    Item 2
    Item 3
    Item 4
### Structure of Table with their description 

#### Item1 table -
It is related to storage of data of item that the company have

| S.NO.         | Column Name   | Data Type | Size | Key | NULL |
| ------------- |:-------------:|:---------:|:----:|:---:|:----:|
| 1      | item_code | Integer | 5 |  | YES |
| 2      | item_name     |   Varchar |  20 || YES |
| 3 | rate      |    Float | 13,2 |  | YES |
| 4 | stock_in_hand    | Integer  |    7 |  | YES | 

#### Item2 table -
It is related to storage of data of customers of company. 

| S.NO.         | Column Name   | Data Type | Size | Key | NULL |
| ------------- |:-------------:|:---------:|:----:|:---:|:----:|
| 1      | customer_code | Integer | 5 |  | YES |
| 2      | customer_name     |   Varchar |  25 || YES |
| 3 | Address      |    Varchar | 30 |  | YES |
| 4 | City    | Varchar  |    20 |  | YES | 
| 5     | State     |   Varchar |  20 || YES |
| 6 | pin_no      |    Integer | 6 |  | YES |
| 7 | phone_no    | Integer  |    15 |  | YES | 

#### Item3 table -
It is related to storage of bill history of sold products.

| S.NO.         | Column Name   | Data Type | Size | Key | NULL |
| ------------- |:-------------:|:---------:|:----:|:---:|:----:|
| 1      | Billno | Integer | 6 |  | YES |
| 2      | customer_type     |   Varchar |  8 || YES |
| 3 | Name      |    Varchar | 25 |  | YES |
| 4 | Date    | Date  |     |  | YES | 
| 5     | item_code     |   Integer |  16 || YES |
| 6 | item_name      |    Varchar | 15 |  | YES |
| 7 | Quantity    | Integer  |    7 |  | YES | 
| 8     | Amount     |   Float |  13,2 || YES |
| 9 | Discount      |    Float | 13,2 |  | YES |
| 10 | Netamount    | Float  |    13,2 |  | YES | 

#### Item4 table -
It is stores data of suppliers of company . 

| S.NO.         | Column Name   | Data Type | Size | Key | NULL |
| ------------- |:-------------:|:---------:|:----:|:---:|:----:|
| 1      | supplier_code | Integer | 5 |  | YES |
| 2      | supplier_name     |   Varchar |  25 || YES |
| 3 | Address      |    Varchar | 30 |  | YES |
| 4 | City    | Varchar  |    20 |  | YES | 
| 5     | State     |   Varchar |  25 || YES |
| 6 | pin_no      |    Integer | 6 |  | YES |
| 7 | phone_no    | Integer  |    15 |  | YES | 

## Set up this project in your System 

Open all the files in this repositry in your ide, i used Netbean IDE here.

Username and Password used by me are "root" and "netbean". So, edit this line of code according to your mysql username and password  

    Connection con = (Connection)DriverManager.getConnection("jdbc:mysql://localhost/practise","root","netbean");
