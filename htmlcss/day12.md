# 1_Introduction to Functions

# Example:-

JavaScript

Function greet(){
    console.log("Hello");
}
greet();

# 2_Function Declaration

//################# Function in JavaScript ############### 


// #############  Basics OF Function ###########
// All Below Are Function Declaration
/*
// Printing data 
// Not convenient to print this way 

console.log("This is console text");
console.log("This is console text");
console.log("This is console text");
console.log("This is console text");
console.log("This is console text");


// So We can make function and just call its function
// Declaration of function:
function printText(){
    console.log("This is console text");
}
// Calling Function / Invoked Function/ Run Function
// Code Reusability
printText();
printText();
printText();

*/
// ###################################################################
/*
function addition(){
  return 2+4;
}
const result = addition();
console.log(result);
*/
// ###################################################################

function addition(num1,num2){
    return num1+num2;
  }
  const result = addition(10,20);
  console.log(result);
  
  // Undefined + Undefined = NAN
  
  function additionofThree(num1,num2,num3){
      return num1 + num2+num3
  
  }
  
  // const sumofThree = additionofThree(10,20); // 10+20+undefined = NAN
  const sumofThree = additionofThree(10,20,30); // 10+20+30 = 60
  console.log(sumofThree);
  
  // ------------------------------------------------
  
  // odd or Even 
  
  // function isEven(num){
  //     if(num % 2 === 0){
  //         return true;
  //     }
  //     return false;
  // }
  
  // ------------------------------------------------
  
  function isEven(num){
  
      return num % 2 === 0;
  }
  
  console.log(isEven(2));
  
  // ------------------------------------------------
  
  function firstChar(str){
      return str[0];
  }
  
  console.log(firstChar("abcdef"));
  
  // ------------------------------------------------
  
  // Create function
  // input : array , target(number)
  // output : index of target present in array
  // linear Search
  
  function linearSearch(arr,target){
      
      for(let i=0;i<arr.length; i++){
          if(arr[i]===target){
              return i;
          }
      }
      return -1;
  }
  const arr = [1,2,3,4,5,6,7,8,9,10];
  const res = linearSearch(arr,10);
  console.log(res);
  
# 3_Function Expression

//################# Function in JavaScript ############### 


// #############  Basics OF Function ###########
// All Below Are Function Expression

// Printing data 
// Not convenient to print this way 
/*
console.log("This is console text");
console.log("This is console text");
console.log("This is console text");
console.log("This is console text");
console.log("This is console text");


// So We can make function and just call its function
// Declaration of function :
const printText = function (){
    console.log("This is console text");
}
// Calling Function / Invoked Function/ Run Function
// Code Reusability
printText();
printText();
printText();

*/

// ###################################################################

// Function Expression 
// we initialize const variable to function
// so addition here expresses function
const addition = function (){
  return 2+4;
}
const result = addition();
console.log(result);

// ###################################################################

// function addition(num1,num2){
//     return num1+num2;
//   }
//   const result = addition(10,20);
//   console.log(result);
  
  // Undefined + Undefined = NAN
  
//   function additionofThree(num1,num2,num3){
//       return num1 + num2+num3
  
//   }
  
  // const sumofThree = additionofThree(10,20); // 10+20+undefined = NAN
//   const sumofThree = additionofThree(10,20,30); // 10+20+30 = 60
//   console.log(sumofThree);
  
  // ------------------------------------------------
  
  // odd or Even 
  
//   const isEven= function (num){
//     if(num % 2 === 0){
//           return true;
//       }
//       return false;
//   }
  
  // ------------------------------------------------
  
const isEven= function (num){
  
      return num % 2 === 0;
  }
  
  console.log(isEven(2));
  
  // ------------------------------------------------
  
// const firstChar =  function (str){
//       return str[0];
//   }
  
//   console.log(firstChar("abcdef"));
  
  // ------------------------------------------------
  
  // Create function
  // input : array , target(number)
  // output : index of target present in array
  // linear Search
  
//  const linearSearch = function (arr,target){
      
//       for(let i=0;i<arr.length; i++){
//           if(arr[i]===target){
//               return i;
//           }
//       }
//       return -1;
//   }
//   const arr = [1,2,3,4,5,6,7,8,9,10];
//   const res = linearSearch(arr,10);
//   console.log(res);
  
  

// Above All are function expression :
// anynomous function --> is assigned const variable
// to call the function .

# 4_Arrow Functions

//################# Function in JavaScript ############### 
/*
Arrow function {()=>} is concise way of writing Javascript 
functions in shorter way. Arrow functions were introduced 
in the ES6 version. They make our code more structured and 
readable.

*/

// #############  Basics OF Function ###########
// All Below Are Arrow Function 

// Printing data 
// Not convenient to print this way 
/*
console.log("This is console text");
console.log("This is console text");
console.log("This is console text");
console.log("This is console text");
console.log("This is console text");


// So We can make function and just call its function
// Declaration of Arrow function :
const printText = () =>{
    console.log("This is console text");
}
// Calling Function / Invoked Function/ Run Function
// Code Reusability
printText();
printText();
printText();

*/

// ###################################################################

// Function Expression 
// we initialize const variable to function
// so addition here expresses function
const addition = ()=>{
    return 2+4;
  }
  const result = addition();
  console.log(result);
  
  // ###################################################################
  
  // const addition =  (num1,num2) =>{
  //     return num1+num2;
  //   }
  //   const result = addition(10,20);
  //   console.log(result);
    
    // Undefined + Undefined = NAN
    
    const additionofThree = (num1,num2,num3)=>{
        return num1 + num2+num3
    
     }
    
    // const sumofThree = additionofThree(10,20); // 10+20+undefined = NAN
     const sumofThree = additionofThree(10,20,30); // 10+20+30 = 60
     console.log(sumofThree);
    
    // ------------------------------------------------
    
    // odd or Even 
    
  //   const isEven=  (num) =>{
  //     if(num % 2 === 0){
  //           return true;
  //       }
  //       return false;
  //   }
    
    // ------------------------------------------------
    // if only one parameter we can remove brackets of num
    // also we can just return without writing return
  
     const isEven = num=>  num % 2 === 0;

//    function isEven(num){
       
//     return num % 2 === 0;
//   }

console.log(isEven(2));

    
    
    console.log(isEven(2));
    
    // ------------------------------------------------
    
  // const firstChar = (str)=>{
  //       return str[0];
  //   }
    
  //   console.log(firstChar("abcdef"));
    
    // ------------------------------------------------
    
    // Create function
    // input : array , target(number)
    // output : index of target present in array
    // linear Search
    
  //  const linearSearch = (arr,target)=>{
        
  //       for(let i=0;i<arr.length; i++){
  //           if(arr[i]===target){
  //               return i;
  //           }
  //       }
  //       return -1;
  //   }
  //   const arr = [1,2,3,4,5,6,7,8,9,10];
  //   const res = linearSearch(arr,10);
  //   console.log(res);
    
    
  
  // Above All are function expression :
  // anynomous function --> is assigned const variable
  // to call the function .
  
  # 5_Callback Functions

  // ########### Call back Function  #############

/*
function myfunc(a){
    console.log(a);
    console.log('hello world');
}
myfunc();
myfunc("abc");
myfunc([1,2,3]);
myfunc({name:"abc",age:22});
*/
//--------------------------------------------------------

/*

function myfunc2(){
    console.log("inside my function 2.");
}

function myfunc(callback){
    // here we have passed function
    // console.log(a);
    // calling the passing parameter function;
    callback();
}
// Passing function as argument inside function
myfunc(myfunc2);

*/
// Above is Example of Call back Function

/*
               ########### Call Back Function ###########
A JavaScript callback is a function which is to be executed 
after another function has finished execution.
 A more formal definition would be -
 Any function that is passed as an argument to another 
 function so that it can be executed in that other function
 is called as a callback function.

*/

//-------------------------------------------------------------------



function myfunc2(name){
    
    console.log("inside my function 2.");
    console.log(`my name is ${name}`);

}

function myfunc(callback){
    // In Call back Function
    // Code execution is done first
    console.log("hello there code is been executed")

    // After execution of above function
    // call back function is executed
    // which is passed as an argument
    callback("Yatin");
}
// Passing function as argument inside function
myfunc(myfunc2);

# 6_Default Parameter
// Default parameters


/*
function addtwo(a,b){
    return a+b;
}

// const ans = addtwo(4,5);
// console.log(ans); //  9

const ans = addtwo(4);
console.log(ans); // NaN ---> 4+ undefined

*/

/*
// Before ES6 (how we handled undefined variables)
function addtwo(a,b){
    if(typeof b === "undefined"){
        b=0;
    }
    return a+b;
}

// const ans = addtwo(4);
// console.log(ans); // 4

*/

/*

//  ES6 (how we handled undefined variables)

// Default Parameters ---> In ES6
function addtwo(a,b=0){
    
    return a+b;
}
// const ans = addtwo(4);
// console.log(ans); // 4


const ans = addtwo(4,8);
console.log(ans); // 12

*/

# 7_Rest Parameter
// rest parameters : 
/*
function myfunction(a,b,c){
    console.log(`a  is ${a}`);
    console.log(`b  is ${b}`);
    console.log(`c  is ${c}`);
}

myfunction(1,3,4);
// printed avaiable parameters
myfunction(1,3,4,4,56,346,34,3,3);
// here rest parameters are not printed
// how to handle them
*/

/*

// Handling above condition with rest parameters

// Used Rest parameter to get rest parameters 
// in form of array which was ignored before
function myfunction(a,b,...c){
    console.log(`a  is ${a}`);
    console.log(`b  is ${b}`);
    console.log(`c  is ${c}`);
}

myfunction(1,3,4);
myfunction(1,3,4,4,56,346,34,3,3);

*/

// Rest Parameter is used
const addAll = (...numbers) =>{
    
    let total = 0;
   
    for(let num of numbers){

        total = total + num;
    }

    return total;
    
}
const ans = addAll(1,2,3,4,5,6,7,8,9,10);
console.log(ans);

/*
The rest parameter syntax allows a function to accept an
 indefinite number of arguments as an array, providing a 
 way to represent variadic functions in JavaScript.

*/

# 8_Hoisting(hoisting_Intro.js)
// Hoisting In JavaScript

/*
    Conclusion Here:
    The Function Declaration is Hoisted
*/

/*

// Accessing function before Initialization :

hello();


// In Case of Function declaration hoisting is working
function hello(){
    console.log("hello world");
}



// In Case of Function expression hoisting is working
// in all case : var, let, const
const hello = function(){
    console.log("hello world");
}
// Error is Thrown : Initialization is After Calling
// here Function is called before it is been intialized 
// and declared

// This is because of Hoisting Concept
// We will learn in Depth afterwards.

*/


/*
// Another Case:

// Accessing var , let and Const before Initialization :


// console.log(hello); // undefined
// var hello = "hello world";
// console.log(hello); // hello world

// console.log(hello); // error: access before initialization
// let hello = "hello world";
// console.log(hello);

// console.log(hello); // error: access before initialization
// const hello = "hello world";
// console.log(hello);

*/

# 9_Lexical Scope

// ################# Lexical Scope ##################################
/*

Lexical scoping in JavaScript
JavaScript uses lexical scoping to resolve the variable 
names when a function is created inside another function.
It determines the function's parent scope by looking at
where the function was created instead of where it was
invoked.

*/

const myvar = "value1";

function myApp(){
     
    function myfunc(){
        // const myvar= "value59";
        console.log("inside myFunc",myvar);
    }
    
    console.log(myvar);
    myfunc();
}

myApp();


/*

Lexical scope is the ability for a function scope to access 
variables from the parent scope. We call the child function 
to be lexically bound by that of the parent function. 
The diagram below outlines the supposed hierarchy that 
the lexical scope maintains in JavaScript.

// https://www.educative.io/answers/lexical-scope-in-javascript

*/


/*
function myApp(){
     
    const myvar = "value1";
    function myfunc(){
        const myvar= "value59";
        console.log("inside myFunc",myvar);
    }
    const myfunc2 = function(){}
    const myfunc3 = () =>{}
    console.log(myvar);
    myfunc();
}
*/

# 10_Block Scope VS Function Scope

// Block Scope Vs Function Scope


/*

// let and const are block scoped
// var is function scoped

{
    // here let is block scoped
    let firstChar = "afafafafa";
    // similar in case of const
    const  name_var = "adadad";
   
} // THE CODE INSIDE THE CURLY BRACKETS IS CALLED BLOCK.

// In Case of Let : variable
// console.log(firstChar);
// uncaught reference error :firstchar is not defined
// cannot access firstChar as it is blockscoped
// and declared as let
// Similarly:
// In Case of const : variable
console.log(name_var);
// uncaught reference error :firstchar is not defined
// cannot access firstChar as it is block scoped
// and declared as const

*/

// ------------------------------------------------------------

/*

{   
    // Blocked Scoped
    const firstname = "yatin";
    console.log(firstname);
}
// Outer Global body scope
const firstname = "siddesh";
console.log(firstname);

*/

//-------------------------------------------------------------

/*
// In case of var

{
    var firstname = "Yatin";
}

{
    console.log(firstname); 
}
console.log(firstname); 
// can be accessed 
// for var whole global scope is function
// var is function scoped
*/
//--------------------------------------------------------------------
// let firstname="abcd"; // case 2:
//can be accessed through lexical scope by
function myApp(){
    if(true){
        var firstname = "yatin"; // case 1: block scoped
        console.log(firstname); // accessed 
    }
    console.log(firstname);
    // case 1:
    // cannot access yatin data as it is block scope
    // and let and const are blocked scope
    // if it was var we would be able to do so.
    // Error as let is function scoped

    // case 2:
    // this access variable by lexical scope 
    // from variable declared in global scope
}
// console.log(firstname);
myApp();
