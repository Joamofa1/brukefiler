# brukefiler
 
# How to install and run app:

- Using terminal clone this repo by this command:
- git clone
```https://github.com/Joamofa1/brukefiler```
- Once the files is in your system, you can open it in IDE of your choice with Maven.
- In the terminal of IDE, type:
- ```mvn clean install```
Then, you can start the StorageDriveApplication.java or in terminal you can type:
- ```mvn spring-boot:run```
Then the embedded server Tomcat, will start the application on ```port 9000```





# schema Database

``` CREATE TABLE IF NOT EXISTS USERS (
  userId INT PRIMARY KEY auto_increment,
  username VARCHAR(20),
  salt VARCHAR,
  password VARCHAR,
  firstname VARCHAR(20),
  lastname VARCHAR(20)
);

CREATE TABLE IF NOT EXISTS NOTE (
    noteId INT PRIMARY KEY auto_increment,
    noteTitle VARCHAR(20),
    noteDescription VARCHAR (1000),
    userid INT,
    foreign key (userid) references USERS(userid)
);

CREATE TABLE IF NOT EXISTS FILE (
    fileId INT PRIMARY KEY auto_increment,
    fileName VARCHAR,
    contentType VARCHAR,
    fileSize VARCHAR,
    fileUploadDateTime DATE,
    userId INT,
    fileData BLOB,
    foreign key (userId) references USERS(userId)
);

CREATE TABLE IF NOT EXISTS CREDENTIAL (
    credentialId INT PRIMARY KEY auto_increment,
    url VARCHAR(100),
    username VARCHAR (30),
    key VARCHAR,
    password VARCHAR,
    userId INT,
    foreign key (userId) references USERS(userId)
);

 ```
