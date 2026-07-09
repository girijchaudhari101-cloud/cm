# 1_dom_createEle.js

# JavaScript

let para = document.createElement("p");
para.innerText = "Hello World!";
document.body.appendChild(para);

Output:-

A new paragraph with the text "Hello World!" is added to the webpage.

# 2_Change Background Color in JavaScript

# CSS:-
*{
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body{
    font-family: sans-serif;
}

main{
    min-height: 100vh;
    display: flex;
    justify-content:center ;
    align-items: center;
    text-align: center;

}

h1{
    padding: 1rem 2rem;
    background-color: #333;
    color: #efefef;
    border-radius: 1rem;

}

button{
    padding: 1rem 2rem;
    font-size: 1.4rem;
    border-radius: 1rem; 
    margin-top: 1rem;
    cursor: pointer;
    border: none;
    outline: none;
    background-color: background 0.4s;
}
button:hover{
    background-color: rgb(214,214,214);
}

# HTML:-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Little Events Demo</title>
    <link rel="stylesheet" href="little-demo.css">
    <script src="./little-demo.js" defer></script>
</head>
<body>
    <main>
        <div class="container">
            <h1> Current Color : <span class="currentColor"> rgb(122,122,122)  </span> </h1>
            <button>Change Background Color</button>
        </div>
    </main>
</body>
</html>

# JavaScript

// Events Little Demo practice

console.log("hello");

const mainButton = document.querySelector(".container button");
// console.log(mainButton);
const body = document.body;
const currentColor = document.querySelector(".currentColor");

function randomColorGenerator(){
    const red = Math.floor(Math.random()*256);
    const blue = Math.floor(Math.random()*256);
    const green = Math.floor(Math.random()*256);

    const randomColor = `rgb(${red},${green},${blue})`;
    return randomColor;
}

mainButton.addEventListener("click",(e)=>{
    //    console.log("you clicked Me!!!");
       const randomColor = randomColorGenerator();
       console.log(randomColor);
       body.style.backgroundColor = randomColor;
       currentColor.textContent = randomColor;
})

# 3_FilterFruits in JavaScript

<!DOCTYPE html>
<html lang="en">          
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
   <style>
    body{
        background-color: aqua;

    }
    .container1{
        height: 100px;
        width: 100px;
        background-color: blue;

    }
   </style>
</head>
<body>

       <div class="container1">
           
       </div>
        <div class="container">
            <h2>Filter Fruits By Type</h2>
            <select id="fruitType">
                <option value="all">All</option>
                <option value="citrus">Citrus</option>
                <option value="berry">Berry</option>
                <option value="stone">Stone Fruit</option>
            </select>
            <button id="filterBtn">Filter</button>
            <ul id="fruitList">
                <!-- Fruits will be displayed here -->
            </ul>
        </div>
        <script>
             
            
       const fruits = [
    { name: "Lemon", type: "citrus" },
    { name: "Blueberry", type: "berry" },
    { name: "Peach", type: "stone" },
    { name: "Orange", type: "citrus" },
    { name: "Strawberry", type: "berry" },
    { name: "Cherry", type: "stone" },
      ];  

            
            const filterButton = document.querySelector("#filterBtn");
            const fruitSelected = document.getElementById("fruitType");
            
           filterButton.addEventListener("click",(e)=>{
                 
                e.preventDefault();
               const selectedType = fruitSelected.value; 

               const filteredFruits = fruits.filter((fruits)=>{
                    
                   if(selectedType === "all"){
                     return fruits;
                   }
                   if(selectedType === fruits.type){
                     return fruits;
                   }

               })
 
          


           const fruitList = document.getElementById("fruitList");
           fruitList.innerHTML = ""; 
           
           
           filteredFruits.forEach((fruit)=>{

            const newli = document.createElement("li");
            newli.textContent = fruit.name;
            fruitList.append(newli);
            
           })
           
          });


           </script>
</body>
</html>

# 4_Responsive_Navbar.js

# CSS:-

body {
  margin: 0;
  padding: 0;
  font-family: Arial, Helvetica, sans-serif;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px;
}

.navbar-logo-image {
  width: 150px;
  height: 75px;
}

.navbar-links {
  margin-left: auto;
  display: flex;
  list-style: none;
}
.navbar-links li {
  margin-right: 15px;
}
.navbar-links a {
  text-decoration: none;
  color: rgb(51, 51, 51);
}

.navbar-menu-icon {
  display: none;
  border: none;
  background-color: transparent;
  font-size: 25px;
  cursor: pointer;
}

@media screen and (max-width: 750px) {
  .navbar-links {
    display: none;
    justify-content: space-around;
    position: absolute;
    top: 86%;
    left: 0;
    width: 95%;
    background-color: rgb(249, 249, 249);
    border: 1px solid #ccc;
    padding: 15px;
  }
  .navbar-links.active {
    display: flex;
    /* flex-direction: column; */
  }

  .navbar-links li {
    margin-bottom: 15px;
  }

  .navbar-menu-icon {
    display: block;
  }
}

# HTML:-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.2.1/css/all.min.css">
<link rel="stylesheet" href="nav.css">
<script src="nav.js" defer></script>
</head>
<body>

<nav class="navbar">
    <section class="navbar-logo">
        <img class="navbar-logo-image" src="https://entrackr.com/storage/2022/04/Newton-image.jpg" alt="newton-school-logo"/>

    </section>
    <ul class="navbar-links">
        <li><a href="#">Home<a/></li>
        <li><a href="#">About<a/></li>
        <li><a href="#">Courses<a/></li>
        <li><a href="#">Contact<a/></li>   
    </ul>
    <section class="navbar-menu">
        <button class="navbar-menu-icon"><i class="fa-solid fa-bars"></i></button>
    </section>
</nav>
</body>
</html>

# JavaScript

const menuIcon = document.querySelector(".navbar-menu-icon");
const navbarLinks = document.querySelector(".navbar-links");

menuIcon.addEventListener("click", function () {
  navbarLinks.classList.toggle("active");
});

window.addEventListener("resize", function () {
  if (window.innerWidth > 750) {
    navbarLinks.classList.remove("active");
  }
});

# 5_Slider in JavaScript

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <style>
      body {
        font-family: Arial, sans-serif;
        text-align: center;
        padding: 50px;
      }

      .font-resizer {
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-bottom: 30px;
      }

      #textContent p {
        font-size: 16px;
      }
    </style>
  </head>
  <body>
    <div class="font-resizer">
      <label for="sizeSlider">Adjust font size:</label>
      <input type="range" id="sizeSlider" min="10" max="72" value="16" />
      <span id="currentSize">Current Size: 16px</span>
    </div>
    <div id="textContent">
      <p>Adjust the slider to see this text change in size!</p>
    </div>
    <script>
      // javascript code goes here

      const sizeSlider = document.getElementById("sizeSlider");
      const textContent = document.getElementById("textContent");
      const currentSize = document.getElementById("currentSize");

      sizeSlider.addEventListener("input", function () {
        const para = textContent.querySelector("p");
        const fontSize = sizeSlider.value + "px";
        para.style.fontSize = fontSize;
        currentSize.textContent = "Current Size: " + fontSize;
      });
    </script>
  </body>
</html>

# 6_Text_Size_Changer.js

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .container {
  max-width: 400px;
  margin: 50px auto;
}

h1 {
  text-align: center;
}

#text {
  font-size: 18px;
  text-align: center;
  margin-bottom: 20px;
}

button {
  
  padding: 10px 20px;
  font-size: 16px;
  margin: 0 10px;
}
    </style>
</head>
<body>
    <div class="container">
        <h1>Text Size Changer</h1>
        
        <p id="text">This is some sample text.</p>
    
        <button id="increaseBtn">+</button>
        <button id="decreaseBtn">-</button>
    
      </div>
      <script>
        // javascript code goes here

const increaseBtn = document.querySelector("#increaseBtn");
const decreaseBtn = document.querySelector("#decreaseBtn");
const textElement = document.querySelector("#text");

increaseBtn.addEventListener("click", increaseFontSize);
decreaseBtn.addEventListener("click", decreaseFontSize);

function increaseFontSize() {
    const currentSize = parseInt(getComputedStyle(textElement).fontSize);
    
    const newSize = currentSize + 2;
    
    textElement.style.fontSize = newSize + "px";
}

function decreaseFontSize() {
    const currentSize = parseInt(getComputedStyle(textElement).fontSize);
    
    const newSize = Math.max(currentSize - 2, 10);
    
    textElement.style.fontSize = newSize + "px";
}
      </script>
</body>
</html>

