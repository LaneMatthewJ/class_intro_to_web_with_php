# CS3010 Final Exam - Practice: 

### True or False (1 point each)

1. It is possible to join tables on more than one condition.  

2. When working with PHP inside of html code, the scripts are written inside of `<php>` `</php>`elements. 

3. POST calls place variables and values in the URL. 

4. Dynamic sites render HTML with a backend language on the server side before serving up the HTML to send to the user.

5. PHP is run on pages with a `.html` file extension.

6. Static websites allow for users to enter information and send it to the backend for processing. 

7. Dictionaries in PHP access their data with the dot operator. 

8. It is possible to store data across multiple pages with session variables.  

9. MySQL is a Document Store type database.  

10. Data from the front end of a website can be sent to the backend by using the form attribute.  

    

### Multiple Choice (4 points each)

1. What would the URL (assuming we're running this locally) be after a user were to click the submit button with the values of: (ASSUMING I ENTERED MATT AND SNORLAX AS VALUES):  

   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <title>
   			index.php
       </title>
     </head>
     <body>
       <form action='somePage.php' method='get'>
         Name: <input type='text' name='name'> <br />
         FAVORITE POKEMON: <input type='text' name='favPokemon' /> <br />
         <input type='submit'>
       </form>
     </body>
   </html>
   ```

   

   - http://localhost:8888/index.php
   - http://localhost:8888/index.php?name=Matt&favPokemon=snorlax
   - http://localhost:8888/somePage.php
   - http://localhost:8888/somePage.php?name=Matt&favPokemon=snorlax 

   

   

2. Given the defined class, which of the below options is how we would create and execute the function  `interrupt`?: 

   ```php
   class KanyeClass {
       function KanyeClass() {
   			echo "My greatest pain in life is that I will never be able to see myself perform live"; 
       }
     	
     	function interrupt() {
         echo "Imma let you finish"; 
       }
   }
   ```

   

   ```php
   $kanye = new KanyeClass();
   $kanye.interrupt(); 
   ```

   

   ```php
   $kanye = new KanyeClass();
   $kanye->interrupt();
   ```

   

   ```php
   $kanye = KanyeClass();
   $kanye->interrupt(); 
   ```

   

   ```php
   $kanye = new KanyeClass("Kanye West");
   $kanye.interrupt(); 
   ```

   

3. Given the below code, how would we access the variables sent from the form? 

   ```html
   <form action='somePage.php' method='post'>
     Name: <input type='text' name='name'> <br />
     FAVORITE POKEMON: <input type='text' name='favPokemon' /> <br />
     <input type='submit'>
   </form>
   ```

   

   ```php
   $userSubmission = $_GET(); 
   ```

   ```php
   $userName = $_GET["name"]; 
   $userPokemon = $_GET["favPokemon"];
   ```

   ```php
   $userName = $_POST["name"]; 
   $userPokemon = $_POST["favPokemon"];
   ```

   ```php
   $userSubmission = $_POST
   ```

   

   

4. What would the output of the below code be? 

   ```php
   function countStuff($variable){
     $wordArray = explode(",", $variable); 
     $numWords = sizeof($wordArray); 
     $totalCount = 0; 
     
     for($i = 0; $i < $numWords; $i++){
   	  $wordLength = 0; 
       $wordLength = strlen($wordArray[$i]);  
       $totalCount += $wordLength; 
       
       echo $wordArray[$i]."<br />"; 
     }
     
     $averageLetters = $totalCount / $numWords; 
     echo "The average letters per word are: ".$averageLetters; 
     
     
   }
   
   $sentence = "a,b,c ,d e, fg";
   
   countStuff($sentence); 
   ```


   


   ```
   a
   b
   c
   d e
    fg
   The average letters per word are: 2 
   ```

   

   ```
   a,b,c
   ,de
   e,
   fg
   The average letters per word are: 3
   ```

   ```
   a,b,c
   d, e
    fg
   The average letters per word are: 4
   ```

   ```
   a,b,c
   ,de
   e,
   fg
   The average letters per word are: 2
   ```

   

   

   

5. What is the output of the following code? 

   ```php
   function printArray($arr) {
     $arrLen = sizeof($arr); 
   
     for($i = 0; $i < $arrLen; $i++){
       echo $arr[$i]." <br />"; 
     }	
   }
   
   
   function arrayManipulation($array){
     $arrLen = sizeof($array); 
     
     for($i = 0; $i < $arrLen; $i++){
       $array[$i] = "OVERWRITE"; 
     }
     
     printArray($array);
     
     return $array
   }
   
   
   
   $flintstones = ["Fred", "Wilma", "Barney", "Betty"]; 
   arrayManipulation($flintstones); 
   printArray($flintstones); 
   ```

   🤷‍♀️

   ```
   OVERWRITE
   OVERWRITE
   OVERWRITE
   OVERWRITE
   Fred
   Wilma
   Barney
   Betty
   ```

   ```
   Fred
   Wilma
   Barney
   Betty
   OVERWRITE
   OVERWRITE
   OVERWRITE
   OVERWRITE
   ```

   ```
   OVERWRITE
   OVERWRITE
   OVERWRITE
   OVERWRITE
   OVERWRITE
   OVERWRITE
   OVERWRITE
   OVERWRITE
   ```

   ```
   Fred
   Wilma
   Barney
   Betty
   Fred
   Wilma
   Barney
   Betty
   ```

   

### Short Answer (5 points each)

For the following questions, assume there exist two tables in a database: 

**author**

| **name**          | **age** |
| :---------------- | :------ |
| Brandon Sanderson | 43      |
| Ursula K. Le Guin | 88      |
| Neil Stephenson   | 59      |
| N.K. Jemisin      | 46      |
| Samin Nosrat      | 39      |
| Margaret Atwood   | 79      |



**books**

| title                 | genre           | publication_date | author            |
| :-------------------- | :-------------- | :--------------- | :---------------- |
| Way of Kings          | Fantasy         | 2010-08-31       | Brandon Sanderson |
| Words of Radiance     | Fantasy         | 2014-03-04       | Brandon Sanderson |
| The Final Empire      | Fantasy         | 2006-07-17       | Brandon Sanderson |
| Elantris              | Fantasy         | 2005-04-21       | Brandon Sanderson |
| Snow Crash            | Science Fiction | 1992-06-01       | Neil Stephenson   |
| Cryptonomicon         | Science Fiction | 1999-01-01       | Neil Stephenson   |
| A Wizard of Earthsea  | Fantasy         | 1968-01-01       | Ursula K. Le Guin |
| Left Hand of Darkness | Science Fiction | 1968-01-01       | Ursula K. Le Guin |
| The Broken Earth      | Fantasy         | 2018-10-02       | N.K. Jemisin      |
| Salt Fat Acid Heat    | Food            | 2017-04-25       | Samin Nosrat      |

1. Write a SQL Query to **obtain all authors** with an age greater than 50: 

   

   

2. Write a SQL Query to **obtain only age** of Margaret Atwood:

   

   

3. Write a SQL Query to **change the age** of Neil Stephenson to 27

   

   

   

4. Write a SQL Query to **enter new data**  with all of below table's data into the author table.
   Jim Butcher (47), and Liu Cixin (56)

   

   

5. Write a SQL Query to **obtain everything** from the author table joined to all data in the books table. 

   

   

   

6. Write a SQL Query to **obtain all fantasy authors and their works**, from the tables.

   

   

   
   

7. What is the output of the following code, **and** what type of data structure is `myContainer`? 

   ```php
   function readWords($variable, $key1, $key2) {
     echo "The first variable is ".$variable["Movie"]; 
     echo "The second variable is ".$variable["TV"]; 
   }
   
   
   
   $myContainer["TV"] = "Teenage Mutant Ninja Turtles"; 
   $myContainer["Movie"] = "Kung Fu Hustle";
   
   readWords($myContainer, "Movie", "TV"); 
   ```

   

   
   

8. Fill in the function `printList` to display each of the names in myList inside of a `<div>` with their respective styling in colorList:

   ```php
   <?php 
   
   function printList($someList, $someColors){
   
     
     
     
     
     
     
   }
   
   $myList = ["Scary", "Baby", "Sporty", "Posh", "Ginger"]; 
   $colorList = ["crimson", "blue", "green", "gray", "firebrick"]; 
   
   printList($myList, $colorList); 
   
   ?>
   ```





### Coding (10 points each)

For the following questions, assume there exists a MySQL database with the following tables: 

ASSUME LOCALHOST

**author**

| **name**          | **age** |
| ----------------- | ------- |
| Brandon Sanderson | 43      |
| Ursula K. Le Guin | 88      |
| Neil Stephenson   | 59      |
| N.K. Jemisin      | 46      |
| Samin Nosrat      | 39      |
| Margaret Atwood   | 79      |



**books**

| title                 | genre           | publication_date | author            |
| --------------------- | --------------- | ---------------- | ----------------- |
| Way of Kings          | Fantasy         | 2010-08-31       | Brandon Sanderson |
| Words of Radiance     | Fantasy         | 2014-03-04       | Brandon Sanderson |
| The Final Empire      | Fantasy         | 2006-07-17       | Brandon Sanderson |
| Elantris              | Fantasy         | 2005-04-21       | Brandon Sanderson |
| Snow Crash            | Science Fiction | 1992-06-01       | Neil Stephenson   |
| Cryptonomicon         | Science Fiction | 1999-01-01       | Neil Stephenson   |
| A Wizard of Earthsea  | Fantasy         | 1968-01-01       | Ursula K. Le Guin |
| Left Hand of Darkness | Science Fiction | 1968-01-01       | Ursula K. Le Guin |
| The Broken Earth      | Fantasy         | 2018-10-02       | N.K. Jemisin      |
| Salt Fat Acid Heat    | Food            | 2017-04-25       | Samin Nosrat      |

**userpass** (USERNAMES ARE UNIQUE)

| username    | password    |
| ----------- | ----------- |
| stephenKing | scaryThings |
| grrm        | sellout4evr |



LOCALHOST

**Database Name: ** myDatabase

**Database User: ** root

**Database Password:** password



1. Using the provided tables, write code to connect to a database and select all data from the Author table and display them in a table.  

   

   

   

   

   

   

   
   

2. Using the provided tables, write code to connect to a database and check a user's password is correct. If the user's password is correct, Make the user's username persistent so that it can be accessed throughout the entire site. **Assume the username and password are coming from a POST method in a form with the names of each being "username" and "password":** 

   

   

   

   

   

   

   

   

   

   

   

   

   

   

3. Using the provided form, write code to take data from the form and upload it into the proper database table (provided)

```html
<!DOCTYPE html>
<html>
  <head>
    <title>
			Enter a new book!
    </title>
  </head>
  <body>
    <form action='somePage.php' method='post'>
      Title: <input type='text' name='title'> <br />
			Author: <input type='text' name='author'> <br />
      Genre: <input type='text' name='genre'> <br />
      Publication Date: <input type='date' name='publication_date'> <br />
      
      <input type='submit'>
    </form>
  </body>
</html>
```















