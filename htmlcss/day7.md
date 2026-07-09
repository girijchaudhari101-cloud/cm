# 1_History_JS

JavaScript is a programming language used to make web pages interactive and dynamic. It was created by Brendan Eich in 1995 at Netscape. It was originally called Mocha, then LiveScript, and finally renamed JavaScript.

Example:
<button onclick="showMessage()">Click Me</button>

<script>
function showMessage() {
  alert("Hello, JavaScript!");
}
</script>

# 2_Starter_JS

Starter JavaScript is the basic setup for writing JavaScript code. JavaScript can be written inside the <script> tag in an HTML file or in a separate .js file.

Example:
<!DOCTYPE html>
<html>
<body>

<h2>Hello JavaScript</h2>

<script>
  console.log("Welcome to JavaScript!");
</script>

</body>
</html>

# 3_Variable_JS

A variable is a container used to store data. In JavaScript, variables are declared using let, const, or var.

Example

let name = "Yash";
let age = 20;

console.log(name);
console.log(age);

# 4_Variable_keyword

Variable keywords are used to declare variables in JavaScript. The three keywords are let, const, and var.

Example:

let age = 20;          
const PI = 3.14;       
var city = "Pune";     

console.log(age, PI, city);

# 5_String_Indexing_JS

String Indexing is used to access individual characters of a string. Index numbers start from 0.

Example:
let name = "JavaScript";

console.log(name[0]);
console.log(name[4]);

# 6_String_methods_JS

String methods are built-in functions used to perform operations on strings, such as changing case, finding text, or extracting parts of a string.

Example:
let name = "JavaScript";

console.log(name.toUpperCase()); 
console.log(name.toLowerCase()); 
console.log(name.length); 

# 7_Truthy_Falsy_JS

Truthy values are treated as true, and Falsy values are treated as false in conditions.

Falsy Values
false
0
"" (empty string)
null
undefined
NaN

All other values are Truthy.

Example:

let name = "";

if (name) {
  console.log("Truthy");
} else {
  console.log("Falsy");
}

# 8_Operators_JS

Operators are symbols used to perform operations on values and variables, such as addition, comparison, and assignment.

Example:

let a = 10;
let b = 5;

console.log(a + b);  
console.log(a > b);  

# 9_Loops_JS

Loops are used to execute a block of code multiple times until a condition becomes false.

Example (for loop)
for (let i = 1; i <= 5; i++) {
  console.log(i);
}