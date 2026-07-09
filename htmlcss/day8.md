# 1_Array_desctructing_JS

Array Destructuring is a feature that allows you to extract values from an array and store them in variables easily.

Example:

let fruits = ["Apple", "Banana", "Mango"];

let [first, second] = fruits;

console.log(first);
console.log(second);

# 2_Array_methods_JS

Array methods are built-in functions used to add, remove, search, or modify elements in an array.

Example:

let fruits = ["Apple", "Banana"];

// Add an element
fruits.push("Mango");

// Remove the last element
fruits.pop();

console.log(fruits);

# 3_Arrays_JS

An Array is a collection of multiple values stored in a single variable. Array elements are accessed using index numbers, starting from 0.

Example
let fruits = ["Apple", "Banana", "Mango"];

console.log(fruits[0]);
console.log(fruits[2]);

# 4_Clone_array

Cloning an array means creating a copy of an existing array. Changes made to the copied array do not affect the original array.

Example
let arr1 = [10, 20, 30];
let arr2 = [...arr1];   // Clone using spread operator

console.log(arr2);

# 5_for_loop_JS

A for loop is used to repeat a block of code a fixed number of times.

Syntax
for (initialization; condition; increment/decrement) {
  // code
}

Example:

for (let i = 1; i <= 5; i++) {
  console.log(i);
}

# 6_While_loop_JS

A while loop executes a block of code as long as the given condition is true.

Example:

let i = 1;

while (i <= 5) {
  console.log(i);
  i++;
}