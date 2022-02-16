# CS 3010 Exam



**Name:**





## Matching

Place each of the following into either `Block` or `Inline` elements (assuming no additional css styling):

```
<a>
<div>
<ul>
<strong>
<pre>
<sup>
<table>
<hr />
<em>
<h3>
```



| BLOCK | INLINE |
| :---- | ------ |
|       |        |
|       |        |
|       |        |
|       |        |
|       |        |
|       |        |
|       |        |

 

## True or False 

1. **li** elements can be either ordered or unordered depending on their parent. ___________________
2. The **DOM** is a javascript representation of a website. _________________
3. It is not possible to render block elements as inline elements. _________________
4. IDs should not be used more than once. ______________
5. CSS Selectors starting with a `.` are for IDs. _________________
6. The border property in css can take in multiple values. ______________
7. The **pre** element will render text as it is typed in the `.html` file. _________________
8. The **src** attribute can only retrive local code.  ______________ 
9. Javascript can only be placed in the **head** of the file. _____________
10. To change one single element's text on a page, it is best to use **document.write('text here')**. _____________



## Multiple Choice

In this section, please select the correct answer. Add your reasoning if you are unsure. 



1. Given the code: 

```html
 <div id='myID'>
    I am a div!
 </div>
 <div>
   I am also a div! 
 </div>
```



Which of the following css selectors would change the background color of the every  div to black (circle one): 

```
 .myID {
   background: 'black';
 }
```



```
 div {
   background: 'black';
 }
```



```
 #myID {
   background: 'black';
 }
```



```
 .myID {
   background: 'blue';
 }
```





2. Given the code: 

```html
 <!doctype html>
 <html>
   <head>
     <script>
       
       /* FUNCTION GOES HERE */
       
     </script>
   </head>
   <body>
    
			<button onClick='callFunc()'>
         Press ME!
     </button>
     
   </body>
 </html>
```



Which of the following will  retrieve the username and password from the user? 

```javascript
const callFunc = function() {
	const details = prompt("Username: ", "Password")
  
  alert("Thank you " + details.username + " for your password " + details.password)
}
```




```javascript
const callFunc = function() {
	const result = confirm("Please enter your username and password")
}
```



```javascript
const callFunc = function() {
	const username = prompt("Username: ")
  const password = prompt("Password: ")
  
  alert("Thank you " + username + " for your password " + password)
}
```




```javascript
const callFunc = function() {
	alert("Please enter your username and password!")
}
```







3. Given the following code: 

```html
<!doctype html>
<html>
  <head>
     <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">
  </head>
  <body>
   	
    <div class='container'>

      <div>  ONE    </div>
      <div>  TWO    </div>
      <div>  THREE  </div>
      <div>  FOUR		</div>

   	<div>    
  </body>
</html>
```



What classes would you use to ensure that each div took up the **entire** page on an large screen screen, but all rendered **two in the same** row on medium screens, and the **entire**  row on a small screen?



```
col col-xs-4 col-md-12 col-lg-3
```



```
col col-md-6 col-lg-3
```



```
col col-sm-6 col-md-12 col-lg-4
```



```
col col-sm-12 col-md-6 col-lg-12
```





4. Given the code: 

   ```html
    <!doctype html>
    <html>
      <head>
        <script>
          
          	const anotherFunction = function(parameter) {
             	if(parameter == 1 || parameter == 'someString'){
                 console.log('GREAT')
               }
   						
             	console.log('AWESOME' + parameter)
           }
          
   				const callFunc = function() {
             	anotherFunction("JOB")
           }
          
        </script>
      </head>
      <body>
       
   			<button onClick='callFunc()'>
            Press ME!
        </button>
        
      </body>
    </html>
   ```



Which of the following would be printied to the console? 

```
GREAT AWESOME
```



```
AWESOME JOB
```



```
GREAT AWESOME JOB
```



```
GREAT JOB
```





5. Given the following code: 

```html
 <!doctype html>
 <html>
   <head>
     <script>
       	
       /* FUNCTION GOES HERE */
       	
     </script>
   </head>
   <body>
    	<button>
        I AM ALSO A BUTTON
     </button>
     
     
			<button id='button' class='buttonClass' onClick='callFunc()'>
         Press ME!
     	</button>
     
     
     	<div id='button' class='buttonClass'>
        I AM A DIV!
     </div>
   </body>
 </html>
```



Which of the following functions would only grab the button?

```javascript
const callFunc = function(){
  var element = document.getElementsByClassName('buttonClass')
}
```



```javascript
const callFunc = function(){
  var element = document.getElementByID('buttonClass')
}
```



```javascript
const callFunc = function(){
	var element = document.getElementById('button')
}
```



```javascript
const callFunc = function(){
	var element = document.getElementsByTagName('button')
}
```







## Short Answer

1. What does DOM stand for?





2. What is the importance of using unique IDs? 





3. Given the code, what is the output? 

```javascript
const doSomething = function(parameter1, parameter2) {
  var newThing = parameter1 + parameter2
  
  return newThing
}



const newNumber = doSomething(5, 3)
const newString = doSomething('Hello', 'There')

console.log('Our new number is: ' + newNumber + 'and our new string is ' + newString)

```







4. Given the code, write some styling to wrap a border around the div so that it looks like the below image (note - the width of the border is not the width of the screen): 

![Screen Shot 2019-07-10 at 12.02.48 PM](/Users/mjlane/Desktop/Screen Shot 2019-07-10 at 12.02.48 PM.png)

```html
<!doctype html>
<html>
  <head>
    <style>
    

      
      
      
    
    </style>
  </head>
  <body>
    <div class='myClass'>
      I am a div! I sure like having a border around me.
    </div>
  </body>
</html>
```







5. Given the code, write a **function** that  **only** takes in the list *myList*, and prints out both **name** and **spice** for each element. 

```javascript
var myList = [
  { name: 'Mel B', spice: 'Scary' },
  { name: 'Emma Bunton', spice: 'Baby' },
  { name: 'Melanie C', spice: 'Sporty' },
  { name: 'Geri Halliwell', spice: 'Ginger' },
  { name: 'Victoria Beckham', spice: 'Posh' },
]

```







6. Given the following code, write in the required code to create a link from the navbar "contact" at line 20  to the bottom element, "contact" :

```html
<!doctype html>
<html>
  <head> 
    <title>Press my buttons!</title>
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">

    <!-- Latest compiled and minified JavaScript -->
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js" integrity="sha384-aJ21OjlMXNL5UyIl/XNwTMqvzeRMZH2w8c5cRVpzpU8Y5bApTppSuUkhZXN0VxHd" crossorigin="anonymous"></script>
  </head>
  <body>
    <nav class='navbar navbar-default'>
      <div class='container'>
        <div class='navbar-header' style='background-color:#f1f1f1'>
          <a href='#' class='navbar-brand'>My Name</a>
        </div>
    
        <ul class='nav navbar-nav navbar-right'>
    
          <li>  <a                     > CONTACT </a>  </li>
        
        </ul>
      </div>
    </nav>
    
    <div>
      Basic Site materials
    </div>
     
    

    
     <div id='contactID'> 
       I am where contact information lives. If you click on the "contact" portion 
     <div>    

  </body>
</html>
```













7. Write a function `callFunc()` that changes the background color and font size of the `<div>` element.

```html
<!doctype html>
<html>
  <head>
    <title> I am a website </title>
  </head>
  <body>
    <p>
      Hello World
    </p>
    <div>
      Isn't web programming really cool? 
    </div>
		
    <script>

      
      
      
    
   
      
      
      
      
      
      
      
      
      
      
    </script>
    
    <button onClick='callFunc()'>
      CHANGE COLORS!
    </button>       
  </body>
</html>
```











8. Write a function to print out each show and characters (note, the character lists are different in length): 

```javascript
const favoriteShows = [
  {
    name: 'Teenage Mutant Ninja Turtles',
    characterList: [  'Leonardo', 'Donatello', 'Raphael', 'Michaelangelo', 'Splinter', 'April', 'Shredder' ]
	}, 
  {
    name: 'Thundercats',
    characterList: [ 'Lion-O', 'Cheetara', 'Panthro', 'Tygra', 'Snarf', 'Mumm-Ra' ]
  }
]
  
  
  

  
    
  
  


  
  
  
  
  
  
  
```







9. What is the output of the following code? 

```html

```



Array at element 2 is 9



1. In the following code, how would you print out favorite food? 

```
var myDetails = {
  name: 'My Name',
  birthday: 'MyBirthday', 
  favoriteFood: 'Pizza', 
}
```



console.log(myDetails.favoriteFood)





1.  In the following code, what  would be stored in `myValue`: 

   ```
   <!doctype html>
   <html>
     <head>
       <title> I am a website </title>
       <style>
         #greyDiv {
            background-color: lightgrey;
         }
   
         .coolClass {
           font-size: 2em;
           font-weight:bold;
         }
       </style>
    </head>
     <body>
       <p class='coolClass'>
         Hello World
       </p>
       <div id='greyDiv'>
         <p>
           You could go visit google if you want by clicking below!
         </p>
         <a href='www.google.com'> Go to google! </a>
       </div>
       <p class='coolClass'>
   			I'm just a boring paragraph.
       </p>
       <div id='greyDiv'>
   			I like to steal IDs!
       </div>
   
       <script>
           const myValue = document.getElementById('greyDiv')
       </script>
     </body>
   </html>
   ```



```
"<div id='greyDiv'>
    <p>
    You could go visit google if you want by clicking below!
    </p>
    <a href='www.google.com'> Go to google! </a>
</div>"
```





1. In the following code, what value would be stored in `myValue`: 

1. ```
   <!doctype html>
   <html>
     <head>
       <title> I am a website </title>
       <style>
         #greyDiv {
            background-color: lightgrey;
         }
   
         .coolClass {
           font-size: 2em;
           font-weight:bold;
         }
         
         
         .bestClass {
           fond-size: 1em; 
           color: black; 
   				font-family: 'Comic Sans MS'
         }
       </style>
    
    </head>
     <body>
       <p class='coolClass'>
         Hello World
       </p>
       <div id='greyDiv'>
         <p>
           You could go visit google if you want by clicking below!
         </p>
         <a href='www.google.com'> Go to google! </a>
       </div>
       <p class='coolClass'>
   			I'm just a boring paragraph.
       </p>
       <div id='greyDiv'>
   			I like to steal IDs!
       </div>
   
       <script>
           const myValue = document.querySelectorAll('p')
       </script>
     </body>
   </html>
   ```



[ p.coolClass, p, p.coolClass ]



- You are welcome to go into more detail if you'd like, but all I'm looking for is that you understand what accesses what. 





1. Write code as to how you would change the class of the value(s) returned in myValue add `bestClass` as a style class. 

```
	for (var i = 0; i < myValue.length; i++)
	{
    myValue[i].classList.add('bestClass')
  }
```









1. In the following code, what value would be stored in `myValue`: 

1. ```
   <!doctype html>
   <html>
     <head>
       <title> I am a website </title>
       <style>
         #greyDiv {
            background-color: lightgrey;
         }
   
         .coolClass {
           font-size: 2em;
           font-weight:bold;
         }
       </style>
    
    </head>
     <body>
       <p class='coolClass'>
         Hello World
       </p>
       <div id='greyDiv'>
         <p>
           You could go visit google if you want by clicking below!
         </p>
         <a href='www.google.com'> Go to google! </a>
       </div>
       <div class='coolClass'>
   			I'm just a boring paragraph.
       </div>
       <div id='greyDiv'>
   			I like to steal IDs!
       </div>
   
       <script>
           const myValue = document.getElementsByClassName('p')
       </script>
     </body>
   </html>
   ```



Null - there is no classname 'p'



1. In the code from the previous question, what document method is required to get this response back: 

   ```
   HTMLCollection(2) [p.coolClass, div.coolClass]
   ```

   

   ```
   const myValue = document.getElementsByClassName('coolClass')
   
   _OR_ 
   
   
   const myValue = document.querySelectorAll('.coolClass')
   ```

   





## Code Analysis

###### styles.css

```
#container {
  display: flex;
  flex-wrap: wrap;
}

.class-one, .class-four {
  width: 100%;
  height: 10vh;
  background: red;
}

.class-two {
  width: 20%;
  height: 80vh;
  background: blue;
}

.class-three {
  width: 80%;
  height: 80vh;
  background: green;
}
```

###### index.html

```
<!doctype html>
<html>
  <head>
    <link rel="stylesheet" href="./styles.css">

  </head>
  <body>
    <div id="container">
      <div class="class-one">

      </div>
      <div class="class-two">

      </div>
      <div class="class-three">

      </div>
      <div class="class-four">

      </div>
    </div>
  </body>
</html>
```

Draw what the user will see in the box below. Label the areas with their colors.

![img](file:///Users/mjlane/Desktop/Screen%20Shot%202019-07-09%20at%2012.35.46%20PM.png?lastModify=1562773527)