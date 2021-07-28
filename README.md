# notes6
notes from ch 6 reading

Javascript
JavaScript (JS) is a lightweight, interpreted, or just-in-time compiled programming language with first-class functions.
  JavaScript is a prototype-based, multi-paradigm, single-threaded, dynamic language, supporting object-oriented, imperative,
and declarative (e.g. functional programming) styles
  standards for JavaScript are the ECMAScript Language Specification (ECMA-262) and the ECMAScript Internationalization API
specification (ECMA-402)
different than java

Inpu output in plain javascript
 This time we are going to see how to get input from the user and combine that with the other two, to create a simple page that can great you.

examples/js/pure_js_greating.html

< html>
< head>
  < title>Hello World</ title>
< /head>
< body> 
First name: < input id="first_name">
Last name: < input id="last_name">
< button id="say">Say hi!</ button>
 < hr>
< div id="result"></ div>
 < script>
function say_hi() {
    var fname = document.getElementById('first_name').value;
    var lname = document.getElementById('last_name').value;
 
    var html = 'Hello <b>' + fname + '</b> ' + lname;
 
    document.getElementById('result').innerHTML = html;
}
 document.getElementById('say').addEventListener('click', say_hi);
</ script>
 </ body>
</ html>
 
  In the JavaScript code we have a function called say_hi. It used the getElementById we have already seen to locate the DOM element 
representing the input element with the id first_name
 The object returned has a method value that will return the text the user has typed in that field.
We use this technique to retrieve the content of both input fields and assign their content to two variables: fname and lname.
Then, using these variable we create an HTML snippet and assign it to a new variable called html.
Then we set the innerHTML attribute as earlier to show the HTML we generated. 
  basically a template would be an HTML snippet with some place holders and then a function call that gets the HTML snippet (the template)
as a parameter, and gets several key-value pairs. The function then returns a new HTML snippet in which the place holders were replaced
by the value of the appropriate key.
  In a similar way, there are many templating system for JavaScript as well. We are going to look at HandlebarsJS, the JavaScript
templating engine.


Javascript variables
three ways to declare a java script variable
1. var
2. let
3. const

Variables are containers for storing data (values)
var x = 5 sets x as 5
like algebra

javascript identifiers
all js variables must be identified with unique names called identifiers
Generl rules:
Names can contain letters, digits, underscores, and dollar signs.
Names must begin with a letter
Names can also begin with $ and _ (but we will not use it in this tutorial)
Names are case sensitive (y and Y are different variables)
Reserved words (like JavaScript keywords) cannot be used as names
case sensitive

Assignment operator
in js = is an assignment operator

JS Data Types
in programming text values are called text strings
strings are written inside double or single quotes, numbers are without quotes

Declaring (Creating) JS Variables
declare a JS variable with var  
Ex: var carname
assign value using =
carname = "Volvo"
or do it together   var carname = "volvo"
Then we "output" the value inside an HTML paragraph with id="demo"
< p id="demo"></ p>
< script>
var carName = "Volvo";
document.getElementById("demo").innerHTML = carName;
</ script>
you can declare many variables in one statement seperated by commas
can span multiple lines

A variable declared without a value will have the value undefined
Redeclaring a variable does not change its value
can do math with variables      var x = 5 + 2 + 3
or add strings       var x = "John" + " " + "Doe"

remember that JavaScript identifiers (names) must begin with:
A letter (A-Z or a-z)
A dollar sign ($)
Or an underscore (_)
Since JavaScript treats a dollar sign as a letter, identifiers containing $ are valid variable names
 Using the dollar sign is not very common in JavaScript, but professional programmers often use it as an alias 
for the main function in a JavaScript library.
  In the JavaScript library jQuery, for instance, the main function $ is used to select HTML elements.
In jQuery $("p"); means "select all p elements".
  Using the underscore is not very common in JavaScript, but a convention among professional programmers 
is to use it as an alias for "private (hidden)" variables


[Go to TOC](https://catdude2000.github.io/reading-notes/)