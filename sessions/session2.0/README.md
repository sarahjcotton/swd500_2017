# HTML and CSS3
  
## Semantic HTML 

- HTML5 offers new HTML elements that are far more descriptive **no more div soup** 
 

```html
<!DOCTYPE html>
<html>
    <head>
    <title>Title</title>
    </head>
    <body>
         <div id="wrapper">  
           
            <header>
                    <h1>An HTML Five Template</h1>
            </header>
            <div id="content">
            
            		<section> </section>
            		<section> </section>
            
            </div> <!-- we can still use divs -->
            <aside>
            
            </aside>
            <footer>  
            </footer>
        </div> <!-- end[wrapper] -->
    </body>
</html>
```


## Web Forms

![](assets/HTML5FORM.jpg)

>> We can now use far more descriptive input types [http://codepen.io/joeappleton18/pen/PGRpVj](http://codepen.io/joeappleton18/pen/PGRpVj)


- Recall that the form elements have an input type attribute: 
	- `<input type="text">`   	
- HTML5 offers more descriptive input types, you can use any of the below input types: 
	- color
	- date
	- datetime
	- datetime-local
	- email
	- month
	- number
	- range
	- search
	- tel
	- time
	- url
   - week

   
#CSS3  

- We're currently on the third incarnation of CSS3 and there are many new features that you may not be familiar with. 

- Some of the more useful features are:

###Gradients 
	
- We can now easily add a gradient to the background property of an element:

**css**

```
.box-item{
   background: linear-gradient(#ffffff, #e8e8e4 99%); 
   
}
```
**html**

```
<div class="box_item"> this is a gradient </div>
```
**result**

<div style="background:linear-gradient(#ffffff, #e8e8e4 99%)"> this is a gradient</div>

	
### Box Shadow 
	
- The box shadow allows the easy implementation of the drop shadow
	
**CSS**
	
```
.box {
 	
 	/* vertical-shadow horizontal-shadow blur */
 	box-shadow: 5px 5px 5px  #888888;
 	width:200px
 	height: 200px    
}
```
	
**HTML**
	
```
<div class="box">
	
	<p>This is a box</p> 
	
</div>
	
```
	


## Better control over targeting elements 

- Rather than give sub elements a class/id to micro target it we can use CSS sectors to target specific elements
- Consider the following html structure:

```html

<div id="block">
	<p> First paragraph</p>
	<p> Second paragraph</p>
	<p> Third paragraph</p>
</div>
```

- If we wanted to make the first and last paragraph text green, we could use the following rules:

```
#block p:first-child {
	color: green;
}

#block p:last-child {
	color: green;
}


```	
	
	
	
## Task 

[Create a non tival HTML page](task.md)





	












