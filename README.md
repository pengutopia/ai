# ai

This is my artificial intelligence side project that I created to practice and expand my knowledge on machine learning and algorithms. 
It uses a MySQL database to store its data and then utilizes the functions and methods I have coded to sort that data out. 
This also gave me practice into working with more advanced data structures, such as Trees and Maps.

## Getting Started

You can clone my repository to a local remote folder within your computer through Git to load my files.

### Prerequisites

You will need Java, MySQL, and Git installed on your computer to work on this project. Currently, I am using the Eclipse IDE to manage and track my Java packages and project. I am using Sequel Pro to manage the contents of my MySQL database as well. 

### Setting Up Your Database

First and foremost, create an empty database.

```
CREATE DATABASE ai_db
```

In the Admin.java file, you should see the following variables:

```
private static String url = ...
private static String user = ...
private static String pwd = ...
```

Configure these settings with the account that you would like the program to be able to use to access the contents of the database. It is preferred that you use the Sequel Pro client to access the database. Refer to the JDBC documentation on writing the correct URL to go to when accessing your database.

### Sequel Pro Connection Details -- Socket
```
Name: localhost
Host: 127.0.0.1
Username: ...
Password: ...
Database: ...
Port: 3306
```
You can connect to the database through SSL also; it is not required.

### Setting Up Commands

Before running the program, deactivate the word learning algorithm within the AIFramework() method, else your code will fail. Follow these steps and set up the following tables:

``` 
CREATE TABLE `greetings` (phrase VARCHAR (255), ID int AUTO_INCREMENT, PRIMARY KEY (ID))
CREATE TABLE `words` (word VARCHAR (255), type int, tense int, ID AUTO_INCREMENT, frequency int, protected int, PRIMARY KEY (ID))
```

Take a look within the AIFramework.java main method. You will see the contingency prompts that I hard-coded.
Before you can use these commands, the word learning algorithm will ask you to identify these words. The words
that are used within the contigency prompts that refer to commands are protected words. Thus,
when you are asked if this word is a protected word, type "y" or "yes".

```
Is this a protected word?
>> yes
```

more to come...
