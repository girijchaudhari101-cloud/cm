# 1_dom_js

// What is DOM ?

// DOM --> Document Object Model :
// 1. OverView .
// 2. How to use.
// 3. depth case study.
console.log(window);
console.log(window.document); // Human readable representation of JS
console.dir(window.document); // JS Object what Browers See.

// With help of Document Object we can Make many Changes 

/*

 # Why DOM is required?

- HTML is used to structure the web pages and Javascript is used to add behavior to our web pages.
 When an HTML file is loaded into the browser, the javascript can not understand the HTML 
 document directly. So, a corresponding document is created(DOM). DOM is basically the 
 representation of the same HTML document but in a different format with the use of objects. 
 Javascript interprets DOM easily i.e javascript can not understand the tags(<h1>H</h1>) in 
 HTML document but can understand object h1 in DOM. Now, Javascript can access each of the 
 objects (h1, p, etc) by using different functions.

# Structure of DOM: DOM can be thought of as a Tree or Forest(more than one tree). 
The term structure model is sometimes used to describe the tree-like representation of a 
document.  Each branch of the tree ends in a node, and each node contains objects  
Event listeners can be added to nodes and triggered on an occurrence of a given event. 
One important property of DOM structure models is structural isomorphism: if any two DOM
 implementations are used to create a representation of the same document, they will create 
 the same structure model, with precisely the same objects and relationships.


# Why called an Object Model?
-  Documents are modeled using objects, and the model includes not only the structure of a document
 but also the behavior of a document and the objects of which it is composed like tag elements 
 with attributes in HTML.



#  Window Object: Window Object is object of the browser which is always at top of the hierarchy.
    It is like an API that is used to set and access all the properties and methods of the 
    browser. It is automatically created by the browser.

# Document object: When an HTML document is loaded into a window, it becomes a document object. 
 The ‘document’ object has various properties that refer to other objects which allow access 
 to and modification of the content of the web page. If there is a need to access any element 
 in an HTML page, we always start with accessing the ‘document’ object. Document object is 
 property of window object.

# Form Object: It is represented by form tags.
# Link Object: It is represented by link tags.
# Anchor Object: It is represented by a href tags.
# Form Control Elements:: Form can have many control elements such as text fields, buttons, 
  radio buttons, checkboxes, etc.

*/

# 2_get_elementby_id.js

//  ##  Select Element by getElementbyID ##

console.log(window); // There is document object present where all the data

console.log(window.document); // Human readable representation of JS
console.dir(window.document); // JS Object what Browers See.

console.log(typeof document.getElementById("main-heading"));
// In Document Object Model --> document object of window object
console.log(document.getElementById("main-heading"));
console.dir(document.getElementById("main-heading"));

 
/* 

 The getElementById() method returns an element with a specified value.

Note: 
Any id should be unique, but:

If two or more elements with the same id exist, getElementById() returns the first.

*/

const headerELement = document.getElementById("main-heading");

// headerELement.style.color= "red"; 

/*

  with help of getElementbyID we can fetch only IDs
*/

# 3_querySelector.js

// Select ELement using QuerySelector :

/*

const mainHeading = document.querySelector("#main-heading");

mainHeading.style.color="red";

*/

const header = document.querySelector(".header");

console.log(header);

const navItem = document.querySelector(".nav-item");

console.log(navItem);
// we will get the first nav-item as output among other three.


// SO in case we want all the nav-items we can use querySelectorAll 
const navItems = document.querySelectorAll(".nav-item"); 
console.log(navItems);
// returns all the nav-items in form of Nodelist 

/* !important 

 -  The querySelector() method returns the first element that matches a CSS selector.
 -  To return all matches (not only the first), use the querySelectorAll() instead.
 -  Both querySelector() and querySelectorAll() throw a SYNTAX_ERR exception if the selector(s) is invalid.

 - The querySelectorAll() method returns all elements that matches a CSS selector(s).
 - The querySelectorAll() method returns a NodeList.
 - The querySelectorAll() method throws a SYNTAX_ERR exception if the selector(s) is invalid


*/

/* 

 We will Study Further in detail :

 ###  The Difference Between an HTMLCollection and a NodeList ###

A NodeList and an HTMLcollection is very much the same thing.

Both are array-like collections (lists) of nodes (elements) extracted from a document. The nodes can be accessed by index numbers. The index starts at 0.

Both have a length property that returns the number of elements in the list (collection).

An HTMLCollection is a collection of document elements.

A NodeList is a collection of document nodes (element nodes, attribute nodes, and text nodes).

HTMLCollection items can be accessed by their name, id, or index number.

NodeList items can only be accessed by their index number.

An HTMLCollection is always a live collection. Example: If you add a <li> element to a list in the DOM, the list in the HTMLCollection will also change.

A NodeList is most often a static collection. Example: If you add a <li> element to a list in the DOM, the list in NodeList will not change.

The getElementsByClassName() and getElementsByTagName() methods return a live HTMLCollection.

The querySelectorAll() method returns a static NodeList.

The childNodes property returns a live NodeList.

*/

# 4_getElebyClass_query...

/*

// get multiple elements using  getElementbyClassname

const navItems = document.getElementsByClassName("nav-item");
// With getElementsByCLassname we get HTMLCollections
console.log(navItems);

// We get HTMLCollections as output 
// Array like Object (means we can do indexing ,but wont get array methods,
// we can iterate on it).
console.log(navItems[0]);
console.log(navItems[1]);
// It is Object
console.log(typeof navItems[2]);
// But Not Array
console.log(Array.isArray(navItems));

*/

// get multiple elements items using querySelectorAll

const navItems = document.querySelectorAll(".nav-item");
// With querySelectorALL we get Nodelist
console.log(navItems);
// Array like Object (means we can do indexing ,but wont get array methods, 
// we can iterate on it).
console.log(navItems[0]);
console.log(navItems[1]);

# 5_change_styles.js

// change styles of Elements :

/*

// const mainHeading = document.querySelector("#main-heading");
const divElement = document.querySelector("div"); // will return the  first div 
console.log(divElement);

// Now we want specific heading 2 inside div with class headline lets say :
const heading2 = document.querySelector("div.headline h2");
console.log(heading2);
console.log(heading2.style);  
// Looking inside style object with many style properties to make changes
heading2.style.color="#fff";

// InCase of changing background-color style of certain element
// We cannot use  - in js 
// heading2.style.background-color="purple"; // throws error
// So what we do is use camelCase
heading2.style.backgroundColor="purple"; 
heading2.style.border = "5px solid black";
heading2.style.padding = "5px";

*/

/*

*/

console.dir(window.document.head.style);
// Access a Style Object
// The Style object can be accessed from the head section of the document,
// or from specific HTML element(s).

# 6_iterate_elements.js

/*

// get multiple elements using  getElementbyClassname

const navItems = document.getElementsByClassName("nav-item");
// With getElementsByCLassname we get HTMLCollections
console.log(navItems);

// We get HTMLCollections as output 
// Array like Object (means we can do indexing ,but wont get array methods,
// we can iterate on it).
console.log(navItems[0]);
console.log(navItems[1]);
// It is Object
console.log(typeof navItems[2]);
// But Not Array
console.log(Array.isArray(navItems));

*/
/*
// get multiple elements items using querySelectorAll

const navItems = document.querySelectorAll(".nav-item");
// With querySelectorALL we get Nodelist
console.log(navItems);
// Array like Object (means we can do indexing ,but wont get array methods, 
// we can iterate on it).
console.log(navItems[0]);
console.log(navItems[1]);

*/




// ################################################################################################
//              Iterate Elements - using  getElementbyClassname / getElementbyTagName
// ################################################################################################



// get multiple elements using  getElementbyClassname / getElementbyTagName
// HTMLCollections




// const navItems = document.getElementsByClassName("nav-item"); 


// HTMLCollections :
// Array Like Object :
// Indexing Use --> can Iterate --> Using loop or index.
// length property
// console.log(navItems.length);

// 1.Simple for loop
// 2.for of loop
// 3.for each --- > cannot use this method to iterate through HTMLCollection.

// // Iteration Through Nav items 
// for(let i = 0; i < navItems.length;i++){
//     console.log(navItems[i]);

// }


/*
// So we Have to solve below problem we have getElementByTagName.

for(let i = 0; i < navItems.length;i++){
    const navItem = navItems[i];
    navItem.style.backgroundColor = "#fff"; // changed
    navItem.style.color = "black"; // No change as text is inside li a i.e anchor tag

}

*/

// const anchorTags = document.getElementsByTagName("a");
// console.log(anchorTags);

// 1.Simple for loop

/*
for(let i = 0; i < anchorTags.length;i++){
    const anchorTag = anchorTags[i];
    anchorTag.style.backgroundColor = "#fff"; // changed
    anchorTag.style.color="green"; // No change as text is inside li a i.e anchor tag
    anchorTag.style.fontWeight="bold"; 

}
*/

/*
// 2.for of loop

for(let anchorTag of anchorTags){
    anchorTag.style.color = "purple";
    anchorTag.style.backgroundColor = "#fff";
    anchorTag.style.fontWeight = "bold";

}

*/

/*

// 3.for each --- > cannot use this method to iterate through HTMLCollection.

anchorTags.forEach((anchorTag)=> {
    anchorTag.style.color = "purple";
    anchorTag.style.backgroundColor = "#fff";
    anchorTag.style.fontWeight = "bold";

});

*/
//-----------------------------------------------------------------------------------------

/*
// But We Resolve Problem 
// By changing HTMLCollections ------------> to Array

// const navItems = document.getElementsByClassName("nav-item"); 
// As we going to change HTMLCollection we are using let instead of const

 let anchorTags = document.getElementsByTagName("a"); 
 
 anchorTags = Array.from(anchorTags);
 
 console.log(Array.isArray(anchorTags)); // True
 // By changing HTMLCollections ------------> to Array
 // We can Use For Each Method now and all the Array Methods.
anchorTags.forEach((anchorTag)=> {
    anchorTag.style.color = "purple";
    anchorTag.style.backgroundColor = "#fff";
    anchorTag.style.fontWeight = "bold";

});

*/



// ################################################################################################
//              Iterate Elements - using  querySelectorAll .
// ################################################################################################


let anchorTags = document.querySelectorAll("a");

console.log(anchorTags);
// querySelectorAll Returns Nodelist

// InCase of NodeList ---- > All 3 works :
// 1.Simple for loop
// 2.for of loop
// 3.for each 

// 1.Simple for loop

/*
for(let i = 0; i < anchorTags.length;i++){
    const anchorTag = anchorTags[i];
    anchorTag.style.backgroundColor = "#fff"; // changed
    anchorTag.style.color="green"; // No change as text is inside li a i.e anchor tag
    anchorTag.style.fontWeight="bold"; 

}
*/

/*
// 2.for of loop

for(let anchorTag of anchorTags){
    anchorTag.style.color = "purple";
    anchorTag.style.backgroundColor = "#fff";
    anchorTag.style.fontWeight = "bold";

}

*/

/*

// 3.for each Method --> can be used in case of NodeList

anchorTags.forEach((anchorTag)=> {
    anchorTag.style.color = "purple";
    anchorTag.style.backgroundColor = "#fff";
    anchorTag.style.fontWeight = "bold";

});

*/


/* Converting Nodelist in Array */

/*
anchorTags = Array.from(anchorTags); // Convert Nodelist --> Array

console.log(Array.isArray(anchorTags)); // True

*/

# 7_dom_traversing.js

# JavaScript

const parent =
document.getElementById("container");
console.log(parent.children);

This code accesses all child elements of the elements with id "container"

# 8_dom_tree.js

 <html>
    <head>
        <title> DOM Traversing</title>
        <script src="dom_tree.js" defer></script>
    </head>
    <body>
        <div class="container">
            <h1>My Heading</h1>
            <p>Some Useful Information .</p>
        </div>
    </body>
    </html>

