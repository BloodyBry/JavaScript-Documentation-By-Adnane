# ⚡ JavaScript Syntax — Variables & Data Types
A quick summary of how to declare variables and understand data types in JavaScript.

```javascript
// =======================
// 1️⃣ Variables
// =======================
let name = "Adnane";   // can be reassigned
const age = 23;        // cannot be reassigned
var city = "Kenitra";  // old syntax (avoid in modern JS)
console.log(name, age, city); // Adnane 23 Kenitra

// =======================
// 2️⃣ Data Types
// =======================
// Primitive Types
let text = "Hello";       
let number = 42;          
let isRunning = true;     
let empty = null;         
let notDefined;           
let unique = Symbol("id");
let big = 12345678901234567890n;
console.log(typeof text, typeof number, typeof isRunning);

// Non-Primitive Types (objects)
let person = { name: "Adnane", age: 23 };
let colors = ["red", "green", "blue"];
function greet() { return "Hello!"; }
console.log(typeof person, typeof colors, typeof greet);

// =======================
// ⚙️ JavaScript Functions
// =======================

// Function Declaration
function greetFn(name) {
  return `Hello YouCode, I'm ${name}!`;
}
console.log(greetFn("Adnane"));

// Function Expression
const greetExpr = function(name) {
  return `Hello, ${name}!`;
};
console.log(greetExpr("Adnane"));

// Arrow Function
const greetArrow = (name) => `Hello, ${name}!`;
console.log(greetArrow("Adnane"));

// =======================
// 🌐 DOM Manipulation — Selecting Elements
// =======================

// Select by ID
const title = document.getElementById("main-title");
console.log(title);

// Select using querySelector
const firstParagraph = document.querySelector(".text");
console.log(firstParagraph);

// Select multiple elements
const allParagraphs = document.querySelectorAll(".text");
console.log(allParagraphs);

// Select by class name
const items = document.getElementsByClassName("item");
console.log(items);

// Select by tag name
const divs = document.getElementsByTagName("div");
console.log(divs);

// =======================
// 🧩 Arrays Manipulation in JavaScript
// =======================

// Declaring Arrays & Getting Size
const fruits = ["apple", "banana", "cherry"];
console.log(fruits.length);

// Adding / Removing Elements
let numbers = [1, 2, 3];
numbers.push(4);
numbers.pop();
numbers.unshift(0);
numbers.shift();

// Iterating Through Arrays
colors.forEach(color => console.log(color));

// Transforming Arrays
const nums = [1, 2, 3];
const doubled = nums.map(n => n * 2);
console.log(doubled);

const ages = [12, 18, 25, 15];
const adults = ages.filter(age => age >= 18);
console.log(adults);

const people = [{ name: "Alice", age: 25 }, { name: "Bob", age: 17 }];
const adult = people.find(person => person.age >= 18);
console.log(adult);

// Sorting & Reducing
const letters = ["d", "a", "c", "b"];
letters.sort();
console.log(letters);

const nums2 = [10, 5, 20];
nums2.sort((a, b) => a - b);
console.log(nums2);

const arr = [1, 2, 3, 4];
const sum = arr.reduce((acc, val) => acc + val, 0);
console.log(sum);

// =======================
// ⚙️ DOM Manipulation — Modifying Elements
// =======================

// Manipulating Content
title.textContent = "Hello World!";
title.innerText = "Welcome Back!";
title.innerHTML = "<span>Hi there!</span>";

// Manage attributes
title.setAttribute("class", "highlight");
console.log(title.getAttribute("class"));

// Adding & Removing Elements
const newDiv = document.createElement("div");
newDiv.textContent = "New Element";
document.body.appendChild(newDiv);

const parent = document.getElementById("container");
const child = document.getElementById("child");
parent.removeChild(child);

const newChild = document.createElement("p");
newChild.textContent = "Replaced!";
parent.replaceChild(newChild, document.getElementById("oldChild"));

// Event Handling
const btn = document.getElementById("myButton");
btn.addEventListener("click", () => alert("Button clicked!"));
document.addEventListener("keyup", e => console.log("Key pressed:", e.key));

// Styling Elements
const box = document.querySelector(".box");
box.style.backgroundColor = "lightblue";
box.style.border = "2px solid black";

// Manage CSS classes
box.classList.add("active");
box.classList.remove("hidden");
box.classList.toggle("highlighted");

// Traversing the DOM
const element = document.querySelector(".item");
console.log(element.parentElement);
console.log(element.children);
console.log(element.nextElementSibling);
