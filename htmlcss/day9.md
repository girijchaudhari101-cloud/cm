# 12_Intro_to_Objects

# 1_dot_bracket.js

// Difference Between Dot and Bracket Notation 

/*
// 1. Difference Case 1 
// (Fetching/Accessing data Through Certain type of Key)


// Here person hobbie key has space in between 
// we cannot store the key without adding string literals
const person = {
    name : "Yatin",
    age : 23,
    "person hobbie" : ["chess","games","sketches"]
}

// In Case of Accessing this type of Key here 
// we need Bracket Notation and not dot 
// as Dot Notation will give error due to space in between

// console.log(person.person hobbie); // invalid error

// For Option is Bracket notation

console.log(person["person hobbie"]);


*/

// 2. Difference Case 2 
// (Adding data )

// created one variable

const key = "email";

const person = {
    name : "Yatin",
    age : 23,
    "person hobbie" : ["chess","games","sketches"]
}

// Dot Notation (adding data with key variable)

// person.key = "abcd2323@gmail.com";
//here while adding data with dot notation
// the key variable it self is considered key here and 
// not the data inside the key 

// Bracket Notation (adding data with key variable)

// person["key"] = "abcd2323@gmail.com";
person[key] = "abcd2323@gmail.com";
console.log(person);

// here when we give key variable it fetches its value and 
// value is assigned as key and to it email data in person object.

# 2_computed_properties.js

// computed properties

const key1 = "objkey1";
const key2 = "objkey2";

const value1="myvalue1";
const value2="myvalue2";

// const obj = {
//     "objkey1" : "myvalue1",
//     "objkey2" : "myvalue2",
// }


// Here we  want to fetch the values of key1 and key2
// for it we need to use computed properties
// just like value1 and value2  fetched its variable data.
// we want  it for keys so just add bracket Notation 
// const obj = {
//     key1 : value1,
//     key2 : value2,
// }

// const obj = {
//     [key1] : value1,
//     [key2] : value2,
// }

// other way

const obj = { };

    obj[key1] = value1,
    obj[key2] = value2


console.log(obj);

# 3_intro_Objects.js

// ################ Introduction to Objects .#############


// Arrays are Good but not sufficient for real world data.


// 1.Object is Reference type
// Stored in Similar to Array in heap and stack pointer 
// pointing ,All Reference type act in same way.

// 2.Objects are Stored in key value pairs
// 3.object dont have index.

// -----------------------------------------------------------

// How to create Objects

// Object created for person
const person = {
    name : "Yatin",
    age : 23,
    hobbie : ["chess","games","sketches"]
}

console.log(typeof person);
// -----------------------------------------------------------

// how to access data from objects (Dot Notation)
console.log(person.name);
console.log(person.age);
console.log(person);
console.log(person.hobbie);

// Accessing with help of key other way (Bracket Notation)
console.log(person["name"]);
console.log(person["age"]);
console.log(person["hobbie"]);
// -----------------------------------------------------------

// how to add key value pair to objects (Dot Notation)
person.gender = "male";
console.log(person);

// adding with help of (bracket Notation)

person["city"]="kalyan";
console.log(person);

// -----------------------------------------------------------


# 4_iterate_objects.js

// How to iterate in Objects
const person = {
    name : "Yatin",
    age : 23,
    "person hobbie" : ["chess","games","sketches"]
}
//-------------------------------------------------------------
// Two Ways To Iterate Through Objects ::

// ###  1. for in loop
// ###  2. Objects.keys

// // Not able to fetch with Dot Notation
// for(let key in person){
//     console.log(person.key);
// }

//-------------------------------------------------------------

// // With help of Bracket Notation
// for(let key in person){
//     console.log(person[key]);
// }

// With help of Bracket Notation key : value pairs

for(let key in person){
    console.log(key," : " ,person[key]);
}

for(let key in person){
    console.log(`${key} : ${person[key]}`);
}
//-------------------------------------------------------------


// Objects.keys(person);

console.log(Object.keys(person));
// Gives Array of Keys
console.log(Object.values(person));
// Gives Array of Values

//-------------------------------------------------------------

console.log(typeof Object.values(person));

// Checking that the Object.Keys and Object.values 
// do they return arrays as values
const val = Array.isArray( Object.values(person));
console.log(val);

//-------------------------------------------------------------

for(let key of Object.keys(person)){
    console.log(key);
}


for(let value of Object.values(person)){
    console.log(value);
}

# 5_nested_destructuring.js

// Nested Destructing


const users = [
    {
    userid : 1,
    user_name: "Yatin",
    gender : "male"},
    {
    userid : 2,
    user_name: "siddesh",
    gender : "male"},
    {
    userid : 3,
    user_name: "shivani",
    gender : "female"},

]

/*
// Here we Destructured Array
// Where we have Objects as Value in it;
const[user1,user2,user3] = users;
console.log(user1);
console.log(user2);
console.log(user3);
*/

// Now These Object also have key value pairs in it 
// how can we destructure it

/*
const[{user_name},,{gender}] = users;
console.log(user_name);
console.log(gender);
*/


// Assigning variable as well
const[{user_name : user1_username,userid},,{gender:user3_gender}] = users;
console.log(user1_username);
console.log(user3_gender);
console.log(userid);

# 6_object_destructuring.js


// #################### Object Destructuring ###################

/*
const band = {
    bandName : "led Zepplin",
    famousSong : "Stairway to heaven",
};

const bandName = band.bandName;
const famousSong = band.famousSong;

console.log(bandName,famousSong);

*/

//  ############ ###########  ############# #############

// Other way to Destructure

/*
const band = {
    bandName : "led Zepplin",
    famousSong : "Stairway to heaven",
};


// First we need to decide we want const let or var
// we want two variables
// const{bandName,famousSong}= band;

console.log(bandName,famousSong);

*/

//  ############ ###########  ############# #############

/*
const band = {
    bandName : "led Zepplin",
    famousSong : "Stairway to heaven",
};


// First we need to decide we want const let or var
// we want two variables
// const{bandName,famousSong}= band;
// bandName = "queen"; //  error --> (we cannot change const)

 let{bandName,famousSong}= band;
bandName = "queen";
// here it is changed

console.log(bandName,famousSong);
*/

//  ############ ###########  ############# #############

/*

const band = {
    bandName : "led Zepplin",
    famousSong : "Stairway to heaven",
    year : 1993,
    othersong: "abcdef",
};

// First we need to decide we want const let or var
// we want two variables
// const{bandName,famousSong}= band;

 let{bandName,famousSong}= band;

console.log(bandName,famousSong);
// Here
// Year key and othersong and its value is in object
// it is not destructured.

*/

//  ############ ###########  ############# #############
/*
const band = {
    bandName : "led Zepplin",
    famousSong : "Stairway to heaven",
    year : 1993,
    othersong: "abcdef",
};

// First we need to decide we want const let or var
// we want two variables
// const{bandName,famousSong}= band;

 let{bandName : var1,famousSong :var2}= band;

console.log(var1,var2);

*/


//  ############ ###########  ############# #############

const band = {
    bandName : "led Zepplin",
    famousSong : "Stairway to heaven",
    year : 1993,
    othersong: "abcdef",
};

// First we need to decide we want const let or var
// we want two variables
// const{bandName,famousSong}= band;

 let{bandName ,famousSong ,...restprops}= band;

 console.log(bandName,famousSong,restprops);

// Adding remaining key value pairs as object in variable.


//  ############ ###########  ############# #############

# 7_object_inside_array.js

// Objects inside Array

// Very Useful in Real world Applications

const users = [
    {
    userid : 1,
    user_name: "Yatin",
    gender : "male"},
    {
    userid : 2,
    user_name: "siddesh",
    gender : "male"},
    {
    userid : 3,
    user_name: "shivani",
    gender : "female"},

]

console.log(users);

// Iterating it :

for(let user of users){
    console.log(user);
    console.log(user.user_name);
    console.log(user.userid);
}

# 8_spread_operator.js

// Spread Operator

/// -------------------------------------------------------------------------------
const arr1 = [ 1,2,3];
const arr2 = [5,6,7];

// const newarr = [...arr1];
// const newarr = [...arr1,...arr2];
// const newarr = [...arr1,arr2]; 
// whole array object added as third element 
// with ... it is spread and then added to elements of new arr
// const newarr = [...arr1,...arr2,82,13];


// const newarr = ["abc"];
// const newarr = [..."abc"];
// Spreading String and adding Each Element 
// On seperate Index
// In Case of Number they are not Iteratable
// we Have String Iterable , Array Iteratable
// const newarr = [...123241244214];
const newarr = [..."123241244214"];
// we can convert it into string and do it

console.log(newarr);

/// -------------------------------------------------------------------------------


// Spread Operator in Objects

// In Object only one key can exist they are unique
// value will override in key if added 
// const obj1 = {
//     key1 : "value1",
//     key2 : "value2",
//     key1 : "value3",
// };
// console.log(obj1);

/// -------------------------------------------------------------------------------


/*

// Cloning in Objects
const obj1 = {
    key1 : "value1",
    key2 : "value2",
};
const obj2 = {
    key3 : "value3",
    key4 : "value4",
};

// const newobj = {...obj1}
const newobj = {...obj1,...obj2};

console.log(newobj);

*/
/// -------------------------------------------------------------------------------


// Even when we clone objects in new Object
// it will override the values if two objects have same key
// But there are two cases according
// to they way there are added and cloned in sequence
const obj1 = {
    key1 : "value1",
    key2 : "value2",
    
};
const obj2 = {
    key1 : "addingUnique",
    key3 : "value3",
    key4 : "value4",
};

// const newobj = {...obj1}
// const newobj = {...obj1,...obj2};

// console.log(newobj);
// case 1:
// Here the key of obj2 will override the key of obj1 
// as it is added afterwards


// const newobj = {...obj2,...obj1};
// console.log(newobj);
// case 2:

// Here the key of obj1 will override the key of obj2
// as it is added afterwards



/// -------------------------------------------------------------------------------
// also we can add new key value pairs

// const newobj = {...obj2,...obj1,key23:"abcd"};

// console.log(newobj);

/// -------------------------------------------------------------------------------

// Using Spread Iterable in String in Object

// const newobj = {..."abcdef"};
// we spread string  and will be saved as key value pair
// console.log(newobj);
/// -------------------------------------------------------------------------------

// Spreading array items with key value pairs
const newobj = {...["item1","item2"]};

console.log(newobj);

# Imp Array Methods..

# 1_ArrayMethods.js

/*
let newarray = [];
console.log(newarray);
console.log(newarray.pop());
console.log(newarray);
*/

// add first unshift
// remove first shift
// add last push
// remove last pop
// concat method to add 2 arrays

// COnvert arr to String
//  replace and replaceAll method
/*
const charArr = ["A", "M", "A", "N"];
const res = charArr.toString().replaceAll(",", "");
console.log(res);
*/

/*
// slice method
// doesnt modify orignal
const num = [1, 2, 3, 4, 5, 6, 7];

// exclusive value taken <2
const res1 = num.slice(2);
// exclusive value taken <4
const res2 = num.slice(0, 4);

// exclusive value taken <2
console.log(res1);
// exclusive value taken <4
console.log(res2);

// splice method
// modifies Original Array
// (start,deletecount,anythingtoAdd)
console.log(num);
num.splice(3, 0, "Abc");
num.splice(3, 2, "krk");
console.log(num);
*/

/*
// join method
const charArr = ["A", "M", "A", "N"];
const res = charArr.toString().replaceAll(",", "/");
console.log(res);
// replacement of above scenario using join
let charStr = charArr.join("/");
console.log(charStr, typeof charStr);

//  includes Method
// indexOf Method --> search from beginning
// lastIndexOf Method --> search from Last

let newArray = ["N", 1, 3, 4, 5, "A", 87];
console.log(newArray.includes("A"));
console.log(newArray.includes(2));
console.log(newArray.indexOf(2));
console.log(newArray.indexOf("N"));
console.log(newArray.lastIndexOf("N"));

// forEach --> ES6 Introduction
// works on array
// doesnt work on object
newArray.forEach((e, index) => {
  console.log(e, index);
});

// forEach
// Doesnt return array
// Only perform operation on array

const newArray1 = newArray.map((e, index) => {
  return e * 3;
});

console.log(newArray1);
// map
// same as foreach
// returns new Array
*/

// =================================================================================

let number = [1, 2, 3, 4, 5, 6, 7, 8, 9];
// filter method
// return new array as output acc to call back condition
const evenArray = number.filter((value, idx) => {
  console.log(value, idx);
  return value % 2 == 0;
});

console.log(evenArray);

let newArray = ["N", 1, 3, 4, 5, "A", 87, { name: "Newton" }];
newArray.forEach((e, index) => {
  if (typeof e === "object") {
    console.log(e, index);
  }
});

//find method
const checkObject = newArray.find((e) => e.name === "Newton");
const checkObjectIndex = newArray.findIndex((e) => e.name === "Newton");
console.log(checkObject);
console.log(checkObjectIndex);

// some --> It will check and return true if one matches in the array

const check = newArray.some((e) => e === "N");
console.log(check);

// every --> It will check all Elements in the array

let StudentsMarks = [45, 64, 77, 45, 54];

const check2 = StudentsMarks.every((e) => {
  return e > 35;
});

console.log(check2);

// reduce

let array = [4, 2, 3, 4, 5, 6, 7];

const newArray2 = array.reduce((accumulator, currentValue) => {
  console.log("acc :  ", accumulator);
  console.log("curr :  ", currentValue);
  return accumulator + currentValue;
}, 10);
console.log(newArray2);

//----------------------------

let x = 10.7;
console.log(parseInt(x));
let y = 10.525;
console.log(Math.floor(y));
console.log(Math.abs(y));
console.log(Math.ceil(y));

let str = "newTono";
let str1 = "school";
console.log(str.length);
console.log(str.slice(0, 2));
console.log(str.charAt(4));
console.log(str.charCodeAt(4)); //ASCII
console.log(str.toUpperCase());
console.log(str.toLowerCase());
console.log(str.substring(2, 5));
console.log(str.replace("n", "M"));
console.log(str.replaceAll("o", ""));
console.log(str.concat(str1));
str = " new  ton ";
console.log(str.trim("//s"));
console.log(str.trimEnd());
console.log(str.trimStart());
str = "newton school";
console.log(str.split(" "));
str = "4";
console.log(str.padStart(5, "0"));
console.log(str.padEnd(5, "0"));

# 2_every_method.js

// ##################### Every Method #####################

/*
   The every() method is an iterative method. It calls a provided 
callbackFn function once for each element in an array, until the 
callbackFn returns a falsy value. If such an element is found, 
every() immediately returns false and stops iterating through the
 array.

*/
const numbers = [2,4,6,8,10];

const ans = numbers.every((number)=>{
    return number % 2 ===0;
})

/// Callback function ---> true / false is returned (boolean).
// Every method ---> true /  false (boolean).

console.log(ans);


//-----------------------------------------------------------------------

// Real world example of Every 


const userCart = [
    {product_Id : 1,product_Name : "mobile", price : 12000},
    {product_Id : 2,product_Name : "TV", price : 22000},
    {product_Id : 3,product_Name : "Laptop", price : 35000},
    {product_Id : 4,product_Name : "charger", price : 1000},

]

const giveDiscount = userCart.every((product)=>{
    return product.price<=35000;
})

console.log(giveDiscount);

// ------------------------------------------------------------------------------

# 3_fill_method.js

// ####################### fill Method ##################################


/*
   he fill() method fills specified elements in an array with a 
   value. The fill() method overwrites the original array. Start 
   and end position can be specified. If not, all elements will be 
   filled.


*/
// Overwrites Original Array

// const myArray =  new Array(10).fill(0);
// console.log(myArray);

// -------------------------------------------------------

const numbers = [1,2,3,4,5,76,6,78,9,9,8];

numbers.fill(0,3,7);
// value , start, end
// 0 will be filled, start from 3rd index, End before 7th index
// [1, 2, 3, 0, 0, 0, 0, 78, 9, 9, 8] // output

console.log(numbers);

# 4_map_method.js

// ################### Map method #####################


// Mostly used in React js
// Works similar to for Each

// Map Method
// Takes call back function as an input
// and returns output in array

const numbers = [4,3,5,6,5];

/*
const sqr = function (number){
    return number * number;
}

const sqrnumber = numbers.map(sqr);
console.log(sqrnumber);
*/


// we can also write it as
/*
const sqrnumber = numbers.map((number)=>{
     
    return number*number;

})
console.log(sqrnumber);
*/

/*
const sqrnumber = numbers.map((number,index)=>{
     
    return `index : ${index},${number*number}`;

})
console.log(sqrnumber);
*/


//-=-------------------------------------------------------------

// mostly real example


const users = [
    {firstName:"Yatin",age : 22},
    {firstName:"mohit",age : 20},
    {firstName:"rajesh",age : 23},
    {firstName:"ramesh",age : 27},
    {firstName:"siddhi",age : 24},
]

const user_names = users.map((user)=>{
    return user.firstName;
})
console.log(user_names);

# 5_splice_Method.js

// ################### Splice Method ##############################//
/*
What is splice method in JavaScript?
The splice() method is a built-in method for JavaScript Array 
objects. It lets you change the content of your array by removing 
or replacing existing elements with new ones. This method modifies 
the original array and returns the removed elements as a new array.
*/

// Changes original array
// Start , delete ,insert

// const array = ['item1' , 'item2','item3','item4','item5'];

// ################ delete using splice ############# 

// input : ['item1', 'item2', 'item3', 'item4', 'item5']

// start from 1st index, delete (how many elements) - 2 
// array.splice(1,2);
// console.log(array);
// output : ['item1', 'item4', 'item5']
// two elements deleted from index 1.

// It also returns deleted Element

// const deletedElement = array.splice(1,2);
// console.log(array);
// console.log(deletedElement);



// ################# insert using Splice #########################


// input : ['item1', 'item2', 'item3', 'item4', 'item5']

// start from 1st ,  delete 0 elements, add from 1st index 
// array.splice(1,0,'newitem');
// console.log(array);
// output : ['item1', 'newitem','item2', 'item3', 'item4', 'item5']


// ############ insert and delete simultaneously ############

const array = ['item1' , 'item2','item3','item4','item5'];

const deletedElements = array.splice(1,2,"insertitem1",'insertitem2');
console.log(array);
console.log(deletedElements);
// return array of deleted items

# 6_sort_method.js


// Sort Method
// Sorting According to ASCII value :
// a to z = 97 to 22
// A to Z = 65 to 90
// o to 9 = 48 to 57

/*
   The sort() sorts the elements of an array.
   The sort() overwrites the original array.
   The sort() sorts the elements as strings in alphabetical
   and ascending order.


*/


// Sort Method Mutates Original Array
// forEach , Map,Filter didnt Change Original Array
// Returns new Array

/*

// 5,9,1200,400,3000
// 5,9,400,1200,3000 (expected output)
const numbers = [5,9,1200,400,3000];
// ["5","9","1200","400","3000"];  // INPUT
// [53,57,49,52,51]
// ["1200","3000","400","5","9"];  // OUTPUT

// '0' : 48
// '1' : 49
// '2' : 50
// '3' : 51
// '4' : 52
// '5' : 53
// '6' : 54
// '7' : 55
// '8' : 56
// '9' : 57
numbers.sort();
console.log(numbers);



// Sorting UserName

const UserNames = ['harshit','abcd','mohit','nitish','aabc'];
UserNames.sort();
console.log(UserNames);

*/

/*
// Then How to get Expected Output 
// Sort Method can also take callback function

const numbers = [5,9,1200,400,3000];

numbers.sort((a,b)=>{
    return a-b;
});

console.log(numbers); 

// 1200 , 400
// a ,b
// a - b
// 1200 - 400 = positive 
// i.e > 0 (greater than  0)
// --> then  b,a
// 400 , 1200

// a-b --> negative ---> a,b
// 5,9 ---> -4
// a ,b 
// 5,9

*/


// Real World Example
// price lowToHigh HighToLow


const products = [
    {product_Id : 1,product_Name : "mobile", price : 12000},
    {product_Id : 2,product_Name : "TV", price : 22000},
    {product_Id : 3,product_Name : "Laptop", price : 35000},
    {product_Id : 4,product_Name : "charger", price : 1000},
    {product_Id : 5,product_Name : "ipad", price : 15000},

]

// Low to High Price

const lowToHigh = products.slice(0).sort((a,b)=>{
   return a.price - b.price;
})

console.log(lowToHigh);

// High to Low Price

const HightoLow = products.slice(0).sort((a,b)=>{
    return b.price - a.price;
 })
 
 console.log(HightoLow);
 
 