Swathi Sundaravarathan Final Project Readme File

**Project Summary:**

    This project is based on the Sports Domain. I am creating a Sports Centre where players can enroll themselves for training. They can also rent the equipments for usage. A player who is an expertise in a game can also be a coach. A coach can train multiple games. A player can undergo multiple training. There are 3 users namely the player, coach and admin. A player can enroll himself for a training or get an equipment for rent. 
    
   Fulfilling requirements of specification: I have created 4 classes- Player , Training , Sports , Coach. Player class has the first name , Last name and Age of the Player. Training class has the type of training and date. Sports class has the attributes - equipment name , game(indoor/outdoor), Manufacturing date(date of lending the equipment), type gives the game type(hockey, tennis etc).

**Design :** 
    SignIn page - has the option to login for current users or new users can create a login.
    
    After logging in the browser goes to the welcome page of the respective user(admin, coach, player)
    
    The coach can access the data of the training schedule and also the players who are enrolled. Coach can modify the enrollement of the games , he can also view or delete them
    
    The player can access his data of the training he has been enrolled, he can also enroll to new game for his coach of choice, player can schedule his training.Player also has the option to view his training and modify them according to their wish
  
    The admin has access to all the data of both coach and player
       

**Requirements (Installation, Compile, Runtime, Database, etc) :**

Please make sure the following are installed
Apache NetBeans Software is Connected with JAVA 8 and JAKARTA EE 8 
MySQL Workbench with database ITMD4515, 
junit jupiter engine version 5.8.1,
apache maven plugin
persistence
bean Validation
Payara Server.



**Screen Captures :**

Login Page:
![image](https://user-images.githubusercontent.com/97709529/167340711-cab179b4-7bb8-4515-a09b-271315fe853d.png)

SignUp Page:
![image](https://user-images.githubusercontent.com/97709529/167340559-264e355a-522a-437c-b382-8c6c13fd8e17.png)

Home Page for Coach:
![image](https://user-images.githubusercontent.com/97709529/167340768-69aaf22e-fa85-46fb-87d8-cb39c806199e.png)

Coach Content Page:
![image](https://user-images.githubusercontent.com/97709529/167340842-da470802-ee34-4479-801a-f5bb433eb62f.png)

Coach who is also a player has player content:
![image](https://user-images.githubusercontent.com/97709529/167340990-87d39c9d-339f-4df9-873b-0e6626fd3a93.png)

Enrollment form for sports:
![image](https://user-images.githubusercontent.com/97709529/167341079-42217e68-fe3a-4a7b-9fcc-506eee4aa6be.png)

Successful enrollment:
![image](https://user-images.githubusercontent.com/97709529/167341121-62690f8b-ee0c-4cc3-a5f0-24d2061c2fb4.png)

Reading a single enrollment:
![image](https://user-images.githubusercontent.com/97709529/167341172-db33b6bc-4c33-4be4-815b-14c28d17813b.png)

Updating an enrollment:
![image](https://user-images.githubusercontent.com/97709529/167341217-b694cd26-b803-4aad-a221-09be915881d8.png)

Deleting an enrollment:
![image](https://user-images.githubusercontent.com/97709529/167341256-7f913516-d794-4e64-ac1c-d7c1c28a48f4.png)

Form for scheduling an training for coach:
![image](https://user-images.githubusercontent.com/97709529/167341298-6f5a7ee4-4f44-4930-a7c0-f28dc9aa99cd.png)

After scheduling the training data is reflected in the player content page:
![image](https://user-images.githubusercontent.com/97709529/167341422-1b0a0f10-4716-4d42-9db8-c01c194297c6.png)

Reading training details:
![image](https://user-images.githubusercontent.com/97709529/167341464-7ee6cdbf-07f8-4e80-9838-047f1f2863cf.png)

Player Welcome page:
![image](https://user-images.githubusercontent.com/97709529/167341522-2c72e471-c3a7-4391-a466-2443c397c559.png)

Admin Welcome Page:
![image](https://user-images.githubusercontent.com/97709529/167341564-78759825-ed74-4eee-a82a-0cbab0090fe1.png)

Admin content:
![image](https://user-images.githubusercontent.com/97709529/167341609-9fad387a-d7f0-4e8e-bdfc-868a5bddddf6.png)


**Expected Results/Known Issues :**

    I have created an extra class named game which can be used for conducting tournaments. this class is for improving the model.
    I have name the attribute which is used to display the lending date of the equipment as the manufacturing date.
    Working Script:
        Username - player1 , password: player1
        Username - coach1 , password: coach1
        Username - player2 , password: player2
        Username - coach2 , password: coach2
        Username - admin , password: admin

**Development Insights :**

This course assisted me in learning about the Java Enterprise Edition standard, security, database persistence, and business and presentation components.
I learned about JPA annotations, JPA Query Language, authentication, and authorisation, among other things.
I'm learning how to create web services using EJB components.

I'm new to the Java profession, but I really like how you presented the fundamentals this semester.
I have no prior knowledge of these notions. I learned a lot after working on this project and going over concepts. In the future, I'd like to delve deeper into Hibernate principles. Thank you very much, prof, for all of your help and effort over the semester. We are honored to be a part of your program.
