# ⚡ JavaScript Syntax — Variables & Data Types
A quick summary of how to declare variables and understand data types in JavaScript.

### 1️⃣ Variables
Variables store data values and are declared using `let`, `const`, or `var`.

```javascript
let name = "Adnane";   // can be reassigned
const age = 23;        // cannot be reassigned
var city = "Kenitra";  // old syntax (avoid using in modern JS)

console.log(name, age, city); // Adnane 23 Kenitra

### 2️⃣ Data Types
Primitive types include strings, numbers, booleans, null, undefined, symbol, and bigint.

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

Non-primitive types include objects, arrays, and functions.

let person = { name: "Adnane", age: 23 }; // object
let colors = ["red", "green", "blue"];    // array
function greet() { return "Hello!"; }     // function

console.log(typeof person);  // "object"
console.log(typeof colors);  // "object"
console.log(typeof greet);   // "function"

### JavaScript Functions

JavaScript functions can be declared in three main ways.
**Function Declaration**
function greet(name) {
  return `Hello YouCode, I'm ${name}!`;
}
console.log(greet("Adnane")); // Hello YouCode, I'm Adnane!

**Function Expression**
const greetExpr = function(name) {
  return `Hello, ${name}!`;
};
console.log(greetExpr("Adnane")); // Hello, Adnane!

**Arrow Function**
const greetArrow = (name) => `Hello, ${name}!`;
console.log(greetArrow("Adnane")); // Hello, Adnane!


### 🌐 DOM Manipulation — Selecting Elements
Select and manipulate HTML elements using JavaScript.

// Select by ID
const title = document.getElementById("main-title");

// Select first element by class
const firstParagraph = document.querySelector(".text");

// Select all elements by class
const allParagraphs = document.querySelectorAll(".text");

// Select by class name
const items = document.getElementsByClassName("item");

// Select by tag name
const divs = document.getElementsByTagName("div");

### Arrays Manipulation in JavaScript
Declare, manipulate, iterate, and transform arrays.

// Declaring arrays
const fruits = ["apple", "banana", "cherry"];
console.log(fruits.length); // 3

// Adding/removing elements
let numbers = [1, 2, 3];
numbers.push(4);
numbers.pop();
numbers.unshift(0);
numbers.shift();

// Iterating
const colors = ["red", "green", "blue"];
colors.forEach(color => console.log(color));

// Transforming arrays
const nums = [1, 2, 3];
const doubled = nums.map(n => n * 2);
console.log(doubled);

const ages = [12, 18, 25, 15];
const adults = ages.filter(age => age >= 18);
console.log(adults);

const people = [{ name: "Alice", age: 25 }, { name: "Bob", age: 17 }];
const adult = people.find(person => person.age >= 18);
console.log(adult);

// Sorting & reducing
const letters = ["d", "a", "c", "b"];
letters.sort();
console.log(letters);

const nums2 = [10, 5, 20];
nums2.sort((a, b) => a - b);
console.log(nums2);

const arr = [1, 2, 3, 4];
const sum = arr.reduce((acc, val) => acc + val, 0);
console.log(sum);


### DOM Manipulation — Modifying Elements
Change content, attributes, styles, and handle events.

// Manipulate content
title.textContent = "Hello World!";
title.innerText = "Welcome Back!";
title.innerHTML = "<span>Hi there!</span>";

// Manage attributes
title.setAttribute("class", "highlight");
console.log(title.getAttribute("class"));

// Add/remove elements
const newDiv = document.createElement("div");
newDiv.textContent = "New Element";
document.body.appendChild(newDiv);

const parent = document.getElementById("container");
const child = document.getElementById("child");
parent.removeChild(child);

const newChild = document.createElement("p");
newChild.textContent = "Replaced!";
parent.replaceChild(newChild, document.getElementById("oldChild"));

// Events
const btn = document.getElementById("myButton");
btn.addEventListener("click", () => alert("Button clicked!"));
document.addEventListener("keyup", e => console.log("Key pressed:", e.key));

// Styles & classes
const box = document.querySelector(".box");
box.style.backgroundColor = "lightblue";
box.style.border = "2px solid black";
box.classList.add("active");
box.classList.remove("hidden");
box.classList.toggle("highlighted");

// DOM Traversing
const element = document.querySelector(".item");
console.log(element.parentElement);
console.log(element.children);
console.log(element.nextElementSibling);
