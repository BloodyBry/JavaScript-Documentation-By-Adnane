# ⚡ JavaScript Syntax — Variables & Data Types
A quick summary of how to declare variables and understand data types in JavaScript.

```javascript
// 1️⃣ Variables
// Variables store data values.
// Declared using let, const, or var.

let name = "Adnane";   // can be reassigned
const age = 23;        // cannot be reassigned
var city = "Kenitra";  // old syntax (avoid using in modern JS)

console.log(name, age, city); // Adnane 23 Kenitra

// 2️⃣ Data Types
// Primitive Types
let text = "Hello";       // string
let number = 42;          // number
let isRunning = true;     // boolean
let empty = null;         // null
let notDefined;           // undefined
let unique = Symbol("id");// symbol
let big = 12345678901234567890n; // bigint

console.log(typeof text);      // "string"
console.log(typeof number);    // "number"
console.log(typeof isRunning); // "boolean"

// Non-Primitive Types (objects)
let person = { name: "Adnane", age: 23 }; // object
let colors = ["red", "green", "blue"];    // array
function greet() { return "Hello!"; }     // function

console.log(typeof person);  // "object"
console.log(typeof colors);  // "object"
console.log(typeof greet);   // "function"


# ⚙️ JavaScript Functions
A quick summary of how to declare and use functions in JavaScript.

javascript
// 1️⃣ Function Declaration
function greet(name) {
  return `Hello YouCode, I'm ${name}!`;
}
console.log(greet("Adnane")); // Hello YouCode, I'm Adnane!

// 2️⃣ Function Expression
const greetExpr = function(name) {
  return `Hello, ${name}!`;
};
console.log(greetExpr("Adnane")); // Hello, Adnane!

// 3️⃣ Arrow Function
const greetArrow = (name) => `Hello, ${name}!`;
console.log(greetArrow("Adnane")); // Hello, Adnane!


# 🌐 DOM Manipulation — Selecting Elements
A quick summary of how to select and manipulate elements in the **Document Object Model (DOM)** using JavaScript.



# 🧩 Arrays Manipulation in JavaScript
A quick summary with examples to understand how to **declare**, **manipulate**, **iterate**, and **transform** arrays in JavaScript.

javascript
// 1️⃣ Declaring Arrays & Getting Size
const fruits = ["apple", "banana", "cherry"];
console.log(fruits.length); // 3

// 2️⃣ Adding / Removing Elements
let numbers = [1, 2, 3];
numbers.push(4); // [1, 2, 3, 4]
numbers.pop(); // [1, 2, 3]
numbers.unshift(0); // [0, 1, 2, 3]
numbers.shift(); // [1, 2, 3]

// 3️⃣ Iterating Through Arrays
const colors = ["red", "green", "blue"];
for (let i = 0; i < colors.length; i++) console.log(colors[i]);
colors.forEach(color => console.log(color));

// 4️⃣ Transforming Arrays
const nums = [1, 2, 3];
const doubled = nums.map(n => n * 2);
console.log(doubled); // [2, 4, 6]

const ages = [12, 18, 25, 15];
const adults = ages.filter(age => age >= 18);
console.log(adults); // [18, 25]

const people = [{ name: "Alice", age: 25 }, { name: "Bob", age: 17 }];
const adult = people.find(person => person.age >= 18);
console.log(adult); // { name: "Alice", age: 25 }

// 5️⃣ Sorting & Reducing
const letters = ["d", "a", "c", "b"];
letters.sort();
console.log(letters); // ["a", "b", "c", "d"]

const nums2 = [10, 5, 20];
nums2.sort((a, b) => a - b);
console.log(nums2); // [5, 10, 20]

const arr = [1, 2, 3, 4];
const sum = arr.reduce((acc, val) => acc + val, 0);
console.log(sum); // 10



# ⚙️ DOM Manipulation

javascript
// 1️⃣ Select by ID
const title = document.getElementById("main-title");
console.log(title); // <h1 id="main-title">Hello</h1>

// 2️⃣ Select using querySelector (CSS selector)
const firstParagraph = document.querySelector(".text");
console.log(firstParagraph); // selects first element with class="text"

// Select multiple elements
const allParagraphs = document.querySelectorAll(".text");
console.log(allParagraphs); // NodeList of all elements with class="text"

// 3️⃣ Select by class name
const items = document.getElementsByClassName("item");
console.log(items); // HTMLCollection of elements with class="item"

// 4️⃣ Select by tag name
const divs = document.getElementsByTagName("div");
console.log(divs); // HTMLCollection of all <div> elements




javascript
// 1️⃣ Manipulating Content
const title = document.getElementById("title");

// Change text
title.textContent = "Hello World!";  // updates text content
title.innerText = "Welcome Back!";   // visible text only
title.innerHTML = "<span>Hi there!</span>"; // adds HTML inside

// Manage attributes
title.setAttribute("class", "highlight");
console.log(title.getAttribute("class")); // "highlight"

// 2️⃣ Adding & Removing Elements
const newDiv = document.createElement("div");
newDiv.textContent = "New Element";
document.body.appendChild(newDiv); // add element to end of body

const parent = document.getElementById("container");
const child = document.getElementById("child");
parent.removeChild(child); // remove an element

const newChild = document.createElement("p");
newChild.textContent = "Replaced!";
parent.replaceChild(newChild, document.getElementById("oldChild"));

// 3️⃣ Event Handling
const btn = document.getElementById("myButton");
btn.addEventListener("click", () => {
  alert("Button clicked!");
});

// Other event examples: mouseover, keyup, change, submit, etc.
document.addEventListener("keyup", e => console.log("Key pressed:", e.key));

// 4️⃣ Styling Elements
const box = document.querySelector(".box");
box.style.backgroundColor = "lightblue"; // inline style
box.style.border = "2px solid black";

// Manage CSS classes
box.classList.add("active");
box.classList.remove("hidden");
box.classList.toggle("highlighted");

// 5️⃣ Traversing the DOM
const element = document.querySelector(".item");
console.log(element.parentElement);        // parent node
console.log(element.children);             // child elements
console.log(element.nextElementSibling);   // next sibling element

