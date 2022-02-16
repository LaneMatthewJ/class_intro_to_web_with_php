# Project 3

In this project, you need to create a database with 3 tables: 

1. Username/Password Table
   1. Username - Text - **PRIMARY KEY**
   2. Password - Text 
      - Extra Credit: use an encryption method to encrypt your passwords. 
2. User Profile Table
   1. Username - text - **PRIMARY KEY**
   2. Admin - boolean
   3. DesiredCategory - text
   4. Bio - text 
3. Quiz Question Table
   1. UUID - int - **PRIMARY KEY**
   2. Question - text
   3. Category - text
   4. DifficultlyLevel - int. (Maybe something between 1-5 or 1-10)
   5. IncorrectAnswer1- text
   6. IncorrectAnswer2- text
   7. IncorrectAnswer3- text
   8. CorrectAnswer - text
      - Extra Credit: find a way to store all incorrect answers in a single column. 



For this project, you need to turn in the queries for the following prompts: 



**INSERTS:**

- Write an insert query to insert multiple questions to the quiz table in one insert. 
- Write an insert query to insert multiple users to the user profile table. 
- Write an insert query to insert usernames and passwords for multiple users. 



**UPDATES**

- Write a query to update an already existing user's bio and desiredCategory. 
- Write a query to update only the difficulty level of a specific quiz question. 
- Write a query to update the username/password for a specific user based off of username. 



**SELECT**

- Write a select query to return only questions and correct answers. 
- Write a select query to return all questions above a specific diffucultly level. 



**JOINs**

- Write select queries to: 
  - Join User Profile table with password table
  - Join User Profile table with Quiz Questions on desired category and filter by difficulty level (included by you).



**DELETE**

- Write a query to delete specific quiz questions based on their category and difficulty level.
- Write a query to delete a user based on username. 





**How to Turn In:** 

Along with your queries above, to export the database, go to the **export ** tab in **phpMyAdmin** and select the **quick** radio button, and the format as **SQL**. Copy paste the SQL code into a .txt document.

**Do this for each table** so that each table has its own file. 

**Include all queries in their own file**. 









