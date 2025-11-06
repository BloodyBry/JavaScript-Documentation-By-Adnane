# ⚡ JavaScript Documentation By Adnane (bloodybry)

### 1️⃣ Variables
Variables store data values and are declared using `let`, `const`, or `var`.

```javascript
let name = "Adnane";   // can be reassigned
const age = 23;        // cannot be reassigned
var city = "Kenitra";  // old syntax (avoid using in modern JS)

console.log(name, age, city); // Adnane 23 Kenitra
```


### 2️⃣ Data Types
Primitive types include strings, numbers, booleans, null, undefined, symbol, and bigint.

```javascript
let text = "Hello";       // string
let number = 10;          // number
let isRunning = true;     // boolean
let empty = null;         // null
let notDefined;           // undefined
let unique = Symbol("id");// symbol
let big = 12345678901234567890n; // bigint

console.log(typeof text);      // "string"
console.log(typeof number);    // "number"
console.log(typeof isRunning); // "boolean"
```
Non-primitive types include objects, arrays, and functions.
```javascript
let person = { name: "Adnane", age: 23 }; // object
let colors = ["red", "green", "blue"];    // array
function greet() { return "Hello!"; }     // function

console.log(typeof person);  // "object"
console.log(typeof colors);  // "object"
console.log(typeof greet);   // "function"
```
### JavaScript Functions

JavaScript functions can be declared in three main ways.
**Function Declaration**
```javascript
function greet(name) {
  return `Hello YouCode, I'm ${name}!`;
}
console.log(greet("Adnane")); // Hello YouCode, I'm Adnane!
```
**Function Expression**
```javascript
const greetExpr = function(name) {
  return `Hello, ${name}!`;
};
console.log(greetExpr("Adnane")); // Hello, Adnane!
```
**Arrow Function**
```javascript
const greetArrow = (name) => `Hello, ${name}!`;
console.log(greetArrow("Adnane")); // Hello, Adnane!
```

### 🌐 DOM Manipulation — Selecting Elements
Select and manipulate HTML elements using JavaScript.
```javascript
// Declaring arrays
const fruits = ["apple", "banana", "cherry"];
console.log(fruits.length); // Prints the number of elements → 3

// Adding and removing elements
let numbers = [1, 2, 3];
numbers.push(4);      // Adds 4 at the end → [1, 2, 3, 4]
numbers.pop();        // Removes the last element → [1, 2, 3]
numbers.unshift(0);   // Adds 0 at the beginning → [0, 1, 2, 3]
numbers.shift();      // Removes the first element → [1, 2, 3]

// Iterating through arrays
const colors = ["red", "green", "blue"];
colors.forEach(color => console.log(color)); // Logs each color

// Transforming arrays
const nums = [1, 2, 3];
const doubled = nums.map(n => n * 2); // Creates new array [2, 4, 6]
console.log(doubled);

const ages = [12, 18, 25, 15];
const adults = ages.filter(age => age >= 18); // Keeps only ages ≥ 18 → [18, 25]
console.log(adults);

const people = [
  { name: "Alice", age: 25 },
  { name: "Bob", age: 17 }
];
const adult = people.find(person => person.age >= 18); // Finds first adult → { name: "Alice", age: 25 }
console.log(adult);

// Sorting and reducing
const letters = ["d", "a", "c", "b"];
letters.sort(); // Sorts alphabetically → ["a", "b", "c", "d"]
console.log(letters);

const nums2 = [10, 5, 20];
nums2.sort((a, b) => a - b); // Sorts numerically ascending → [5, 10, 20]
console.log(nums2);

const arr = [1, 2, 3, 4];
const sum = arr.reduce((acc, val) => acc + val, 0); // Adds all numbers → 10
console.log(sum);

```

### DOM Manipulation — Modifying Elements
Change content, attributes, styles, and handle events.
```javascript
// 🧱 Manipulate content
title.textContent = "Hello World!";       // Changes the text inside the element (no HTML)
title.innerText = "Welcome Back!";        // Similar to textContent but respects CSS (like hidden text)
title.innerHTML = "<span>Hi there!</span>"; // Inserts HTML inside the element

// ⚙️ Manage attributes
title.setAttribute("class", "highlight");   // Sets or updates the 'class' attribute
console.log(title.getAttribute("class"));   // Gets and logs the value of the 'class' attribute

// ➕➖ Add or remove elements
const newDiv = document.createElement("div"); // Creates a new <div> element
newDiv.textContent = "New Element";           // Adds text inside the new div
document.body.appendChild(newDiv);            // Adds the div to the end of the <body>

const parent = document.getElementById("container");
const child = document.getElementById("child");
parent.removeChild(child);                    // Removes a child element from its parent

const newChild = document.createElement("p"); // Creates a new <p> element
newChild.textContent = "Replaced!";
parent.replaceChild(newChild, document.getElementById("oldChild")); // Replaces one child with another

// 🖱️ Events
const btn = document.getElementById("myButton");
btn.addEventListener("click", () => alert("Button clicked!")); // Runs function when button is clicked
document.addEventListener("keyup", e => console.log("Key pressed:", e.key)); // Logs key pressed by user

// 🎨 Styles & classes
const box = document.querySelector(".box");
box.style.backgroundColor = "lightblue";  // Changes background color
box.style.border = "2px solid black";     // Adds a border
box.classList.add("active");              // Adds a CSS class
box.classList.remove("hidden");           // Removes a CSS class
box.classList.toggle("highlighted");      // Adds/removes class depending on its current state

// 🧭 DOM Traversing
const element = document.querySelector(".item");
console.log(element.parentElement);       // Logs the parent element
console.log(element.children);            // Logs all child elements
console.log(element.nextElementSibling);  // Logs the next sibling element

```