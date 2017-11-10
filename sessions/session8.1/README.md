

# JavaScript Refresher 

- [Variables](#variables)
- [Including external JavaScript files](#including-external-javascript-files)
- [Running JavaScript](#running-javascript)
- [Variables](#variables)
- [Rules for JavaScript Variables](#rules-for-javascript-variables)
- [Maths operators](#maths-operators)
- [Accessing the dom](#accessing-the-dom)
- [Conditional Statements](#conditional-statements)





# Including external javaScript files 

Just like with CSS it's considered good practice to separate the javaScript code from our HTML. The `<script>` tag allows us to utilise the `src` attribute to include javaScript contained in an external file.   The following conventions must be adhered to:


* The external file should have a `.js` extension
* You do not need to use the `<script>` tag in the external `.js` file 

> **Below we include demo\_script_src.js which lives int he `scripts` folder**  

```html
<html>
<head>
	<script type="text/javascript" src="scripts/demo_script_src.js"></script>
</head>
<body>
  ....
</body>
```

# Running JavaScript 

Once we've included a java script file, we some way of running it. 

- We can include an inline event listener that calls a function that's in an included java script file

```html 
<head>
    <meta charset="UTF-8">
    <script src="scripts/main.js"></script>
    <title>Document</title>
</head>
<body onLoad="run()">
    
</body>
</html>

```

- The above script calls a `run()` function in `main.js` when the html document loads 

**main.js**

```html
function run(){
    
  alert('hello world');   
}
  
```

# Variables 

Computer programs use variables to store information.

#Rules for JavaScript Variables

- Variable names are case sensitive e.g. `y and Y are different`
- Variable names must begin with a letter or underscore e.g. `year, _month`

### Declaring JavaScript Variables

- In JavaScript variables can be declared in the following ways:

	- `var x;` 
	- `var x=5`
	- `var firstNumber,secondNumber,number1,number2,sum;`

# Strings 

- We can concatenate (join together) multiple string by using the `+` operator. 

```html

var first_var = "hello";
var second_var = "world";
var third_var = first_var + second_var;

console.log(first_var + second_var); //hello word printed to the console. 

```

## Converting a string to integer

- If you need to perform comparision or run arithmetic on a sting you'll need to an integer, you can use `passInt()`

```html
var age_string = "18";
var age_int = passInt(age_string);
```



# Maths Operators 

You can apply mathematic operations to numbers using some basic operators like:

```html
 	var x = 5;  
 	var y = 20;  
 	var result = x + y; // result will equal 25
 	var result = x * y; // result will equal 100 
 	var result = y/x;  //  result will equal 5

```

If you want to increment/decrement a variable you can use `++` or `--` respectively:

```html

var x = 10;

x--; //x is now 9
x++; //x is now 10

```


# Accessing the DOM 

- DOM stands for document object model, it's structure that holds our HTML
- We can use the `document.querySelector` to target and manipulate `dom` elements
- Consider the following example:

**html**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <script src="scripts/main.js"></script>
    <title>Document</title>
</head>
<body onLoad="run()">
      
      <p> Enter your name: <input type="text" name="your_name"> </p>
      <button id="click" value=""> Click</button>
      <p id="display_name"></p>
        
   
</body>
</html>

```

**javascript**

```html
function run(){
    
  document.querySelector('#click').addEventListener('click', sayHi);  
}
    

function sayHi() {
      
    var name = document.querySelector('input[name="your_name"]').value;
    document.querySelector('#display_name').innerHTML = "Hello" + " " + name
    
    
}

```

- In the above example, we:

	-`document.querySelector('#click')`. use the query target and then add a click [event listener](https://sirus21.gitbooks.io/internet_technology_block_2/content/session13/event_listener.html) to the button. `#click` is the id of our button. Notice how the second argument of the event listener is the function that will get called when that event is triggered
	-  `document.querySelector('input[name="your_name"]')`. within the function we again use the query selector, this time targeting our input with the name `your_name`. 
	-  Finally we use the query selector to set the inner html of a paragraph with a id of `#display_name` to our message

#Conditional Statements 

In order to code decisions into our javaScript programs it's necessary to use conditional statements know as `if` statements. 

An `if` statement is a
conditional statement which checks to see if a statement is `true`
or `false` and then executes some additional statements depending
on the result.

In javaScript a basic IF statement looks as follows:

```javascript
if (condition) { 
	//code to be executed if condition is true 
}
```
**A real example**

```javascript

//check if the statement 5 > 3 is true and if so
//then print a suitable message
	if (5 > 3){
		console.log("It is bigger!"); 
   }

```

We can also specify an alternative by using an `else` as follows:

```javascript
if (5 > 3){
		console.log("It is bigger!"); 
}else {
		console.log("It is smaller");

}
```
The bigger than symbol `>` is know as a comparison operator.  You may want to make use of the following operators:

|Operator | Description |
|---------|  -----------|
|==|equal to|
|!=|not equal|
|>|greater than|
|<| 	less than|
|>=|greater than or equal to|
|<=|less than or equal to||


We can only have 1 else with every if. If we want to specify more than one alternative then we have to use `else if`. 

Consider the following example:

```javascript 

if (role == "Teacher")
	console.log("You are a teacher!");
}
else if (role == "Student"){
	console.log("You are a student!");
}
else if (role == "Admin"){
	console.log("Your are an admin");
}
else{
	 console.log("I don’t know what you are!");
}
```

In the above example you will notice that an `else if` statement is used
to specify alternative paths and that you can have more than 1 `else if`
statement. In fact, you can have as many `else if` statements as you
like


#Practical 

[Creating A JavaScript guessing game](task.md)