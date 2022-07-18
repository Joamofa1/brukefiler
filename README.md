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

## ScreenView 😜
![screen.mp4](https://github.com/Joamofa1/brukefiler/blob/main/Screen.mp4)



# schemma Database

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



 ```
