# CS3010 Final Exam

**Name:**

### True or False (1 point each)

1. UPDATE statements can only set one variable per update.

2. Dynamic websites can process information by working with data sent from HTTP Requests via forms

3. In order for php to work with HTML, it must be inside `<?php … ?>`. 

4. MySQL is a relational database management system. 

5. All variables in PHP are declared with `var`

6. Arrays in PHP are passed by reference in functions. 

7. When sending data from a front end to a back end, the type of HTTP request is determined by the `action` attribute. 

8. GET calls store variables in the URL. 

9. In MySQL tables, primary keys are not required to be unique. 

10. Dictionary elements are accessed by a numerical index. 

  ​    

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
       <form action='somePage.php' method='post'>
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

   

   

2. Given the code below, how would we define a class that has the variable "spiceLevel"?: 

   ```php
   class BuffaloWings {
       function BuffaloWings() {
   			echo "These wings are spicy";
         $spiceLevel = "fire";
       }
   }
   ```

   ```php
   class BuffaloWings {
     	$spiceLevel = "fire";
       function BuffaloWings() {
   			echo "These wings are spicy";
       }
   }
   ```

   ```php
   class BuffaloWings {
     	$this.spiceLevel = "fire"; 
       function BuffaloWings() {
   			echo "These wings are spicy";
       }
   }
   ```

   ```php
   class BuffaloWings {
       function BuffaloWings() {
   			echo "These wings are spicy";
         $this->spiceLevel = "fire";
       }
   }
   ```

   

   

   

   

3. Suppose the following code is in the file `functions.php`, how would we access it in another file (assuming the files are in the same directory)?

   ```php
   function sayHello($var){
     echo "Hello ".$var."<br />"; 
   }
   ```

   

   

   ```php
   #include functions.php;
   sayHello(" there"); 
   ```

   ```php
   <?php
     import functions.php; 
   	sayHello(" there"); 
   ?>
   ```

   ```php
   <?php
     include "functions.php"; 
   	sayHello(" there"); 
   ?>
   ```

   ```php
   import "functions.php"; 
   sayHello(" there"); 
   ```

   

   

   

   

   

   

   

   

   

   

   

4. What would the output of the below code be? 

   ```php
   function printDictionaryElements($arrayOfKeys, $dictionary){
   	for($i = 0; $i < sizeof($arrayOfKeys); $i++){
   		$someKey = $arrayOfKeys[$i]; 
       $dictionary[$someKey]= $i; 
     }
     
     return $dictionary; 
   }
   
   $keyArr = array("stuff", "things", "stuffAndThings");
   $myDict["book"] = "Amazing"; 
   
   $myDict = printDictionaryElements($keyArr, $myDict); 
   echo $myDict["stuffAndThings"]; 
   ```

   

   ```
0
   ```

   ```
1
   ```
   
   ```
   2
   ```
   
   ```
   Amazing
   ```
   
   




















5. What is the output of the following code  (note: **formatting is important**)? 

   - Assume code will be run in a browser: 
   
   ```php+HTML
   <!DOCTYPE html>
   	<html>
       <body>
         <div>
         <?php 
         	$div = "<div>"; 
           $closeDiv = "</div>"; 
           
           $buggyArray = array('dragonfly', 'lightning bug', 'assassin bug', 'butterfly', 'ladybug', 'grasshopper'); 
           
           for ($i = 0; $i < sizeof($buggyArray); $i++){
             echo $div.$buggyArray[$i].$closeDiv; 
           }
         ?>
         </div>
       </body>
   </html>
   ```
   
   
   
   ```
   <div>dragonfly</div><div>lightning bug</div><div>assassin bug</div><div>butterfly</div><div>ladybug</div><div>grasshopper</div>
   ```
   
```
   dragonfly lightning bug assassin bug 
butterfly ladybug grasshopper
   ```
   
   ```
   <div>dragonfly</div>
   <div>lightning bug</div>
   <div>assassin bug</div>
   <div>butterfly</div>
   <div>ladybug</div>
   <div>grasshopper</div>
   ```

   ```
   dragonfly 
   lightning bug 
   assassin bug 
   butterfly 
   ladybug 
   grasshopper
   ```
   
   

### Short Answer (5 points each)

For the following questions, assume there exist two tables in a database (table data can be found on the final page of this exam): 

1. Write a SQL Query to **obtain all persons** who live in tower grove: 

    

   

3. Write a SQL Query to **change the neighborhood** of Mac's Local Eats  to "Cherokee": 

   

  

5. Write a SQL Query to **remove**  all restaurants that exist in University City:  

   

   

4. Write a SQL Query to **add the new restaurants **below:  

   - Fork 'n Sticks, in University City

   - Olio in Botanical Heights

     

     

   
  
   
5. Write PHP code to access data sent from the below form: 

   ```php+HTML
   <!DOCTYPE html>
   <html>
     <head>
       <title>
   			Enter a new book!
       </title>
     </head>
     <body>
       <form action='somePage.php' method='post'>
         Restaurant: <input type='text' name='restaurantName'> <br />
   			Location: <input type='text' name='location'> <br />
         Type: <input type='text' name='type'> <br />
         
         <input type='submit'>
       </form>
     </body>
   </html>
   ```

   

   

   

   

   

   

6. Fill in the code to update the array so that values of myList change outside of the function. 

   ```php
   <?php 
   
   function updateArray($someArray){
   
     
     
     
     
     
     
   }
   
   $myList = ["Hello", "There", "General", "Kenobi"]; 
   
   						updateArray($myList; 
   
   ?>
   ```

   

7.  What is the output of the following code: 

   ```php
   function myFunc ($var) {
   	for($i = 0; $i < sizeof($var); $i++){
       echo strlen($var[$i])."<br />"; 
     }
   }
   
   
   $myArray = array('o', 'my', 'gosh', 'becky'); 
   myFunc($myArray); 
   ```

   

   

   

   
   
8. Why is it important to close your db connections?

   

   

   

   

   

   

  
  
  
  
  
  
   

### Coding (10 points each)

For the following questions, assume there exists a MySQL database with the following tables: 

1. Write two separate sections of code: 

   - In your first section, write a navbar that uses bootstrap stylings.   
   - In your second section, write a main page that pulls in your navbar at the top of the page. 

    

    

    

    

    

    

   

   

   

   

   

   

   

   

   

   

    

2. Write two separate sections of code: 

   - In your first section, write a form to take in a username and password. 
   - In your second section, write the method to log into the website (be sure to make your username persistent if the username exists)

    

    

    

    

    

    

    

    

    

    

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   
   

    

    

3. Using the provided table data, assume you've already logged in with the above code and: 

   - Obtain a username from persistent data.

   - Query the database to obtain all restaurants that exist in that specific user's neighborhood.

     

     















































**Database Name: ** myDatabase

**Database User: ** root

**Database Password:** password



**person**

| **name** | neighborhood     |
| :------- | :--------------- |
| Sandra   | Central West End |
| Mica     | Tower Grove      |
| Cecily   | South County     |
| Natalie  | University City  |
| Matt     | Tower Grove      |
| Erin     | The Hill         |
| Kelsey   | Tower Grove      |



**restaurants**

| name             | type            | neighborhood     |
| :--------------- | :-------------- | :--------------- |
| The Vine         | Lebanese        | Tower Grove      |
| Taste            | New American    | Central West End |
| Seoul Taco       | Korean Fusion   | University City  |
| Tai Ke           | Taiwanese       | University City  |
| Anis             | Indian          | Maryland Heights |
| Lulu's Lil Eats  | Vegan Soul Food | Tower Grove      |
| Steve's Hot Dogs | Hot Dogs        | The Hill         |
| Mac's Local Eats | Burgers         | Dogtown          |
| The Mud House    | Cafe            | Cherokee         |








**userpass** (USERNAMES ARE UNIQUE)

| username | password    |
| :------- | :---------- |
| Matt     | password    |
| Natalie  | plantsRCool |
| Kelsey   | b0tany4Eva  |
| Mica     | pizzaF4N    |