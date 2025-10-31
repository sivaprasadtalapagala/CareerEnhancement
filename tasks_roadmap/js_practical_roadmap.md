===============================> Level 1 — Environment Setup & First App

🧩 (9) Understand JavaScript engines (V8, Node.js)

Let’s imagine JavaScript as a language, just like English.

But your computer doesn’t understand English or JavaScript directly — it only understands machine language (0s and 1s).

So, something needs to translate JavaScript code into a language the computer understands.
That translator is called a JavaScript engine.

🧠 What is a JavaScript Engine?

A JavaScript Engine is a program inside your browser (like Chrome, Firefox) that reads and runs your JavaScript code.

Example:

console.log("Hello!");


When you run this:

The engine reads your code (console.log("Hello!"))

It translates it into machine code.

Your computer executes it and prints Hello! on the screen.

⚙️ Types of JavaScript Engines

V8 Engine → Used in Google Chrome and Node.js
(Created by Google)

SpiderMonkey → Used in Mozilla Firefox
(Created by Mozilla)

JavaScriptCore (Nitro) → Used in Safari
(Created by Apple)

All these engines do the same job:
👉 They run JavaScript code inside browsers.

🚀 What is Node.js then?

Node.js is not a browser — it’s a runtime environment that uses the V8 engine (the same one Chrome uses).

✅ Browser: Runs JavaScript on websites (in the frontend).
✅ Node.js: Runs JavaScript on your computer or server (in the backend).

That means:

You can use JS for websites (via browser)

Or use JS for servers (via Node.js)

💻 (10) Explore browser console for JS testing

The browser console is like a small playground where you can write and test JavaScript code directly — no setup needed.

🪟 How to open it

Open Google Chrome

Press F12 or Ctrl + Shift + I (Windows)
or Cmd + Option + I (Mac)

Click the Console tab

You’ll see a blinking cursor like this:

>


Now you can type JavaScript directly:

console.log("Hello, World!");


and press Enter → You’ll see:

Hello, World!


You can also test calculations:

5 + 10   // gives 15


Or write simple logic:

let name = "Siva";
console.log("Welcome " + name);




===============================> Level 2 — JavaScript Basics

🧱 (1) Declare variables

Variables are like containers that hold information (like names, numbers, etc.)

Example:

let name = "Siva";
const age = 25;
var city = "Hyderabad";

a) var, let, const
Keyword	Can change value?	Scope	Example
var	✅ Yes	Function-level	Old way (avoid using now)
let	✅ Yes	Block-level	Modern, preferred way
const	❌ No	Block-level	For values that never change

Example:

var x = 10;   // can be changed
let y = 20;   // can be changed
const z = 30; // cannot be changed

b) Scope differences

Think of scope as “where your variable is visible.”

var → works everywhere inside a function

let / const → works only inside curly brackets {}

Example:

{
  let a = 10;
  var b = 20;
}
console.log(b); // ✅ Works
console.log(a); // ❌ Error — only inside block

🔢 (2) Data types

JavaScript can store different types of data:

Type	Example	Description
String	"Hello"	Text values
Number	25, 3.14	Numbers
Boolean	true or false	Yes/No type
Null	null	Empty or nothing
Undefined	undefined	Not assigned yet
Symbol	Symbol('id')	Unique value (advanced concept)

Example:

let name = "Siva";        // String
let age = 25;             // Number
let isStudent = true;     // Boolean
let city = null;          // Null
let country;              // Undefined
let id = Symbol("id");    // Symbol

🧮 (3) Operators
a) Arithmetic Operators

Used for math:

let x = 10;
let y = 3;

console.log(x + y); // 13
console.log(x - y); // 7
console.log(x * y); // 30
console.log(x / y); // 3.33
console.log(x % y); // 1 (remainder)

b) Comparison Operators

Used to compare values.

Operator	Meaning	Example	Result
==	Equal (only value)	5 == '5'	✅ true
===	Strict equal (value + type)	5 === '5'	❌ false
!=	Not equal	5 != 4	✅ true
!==	Strict not equal	5 !== '5'	✅ true
c) Logical Operators
Operator	Meaning	Example	Result
&&	AND	(x > 5 && y < 10)	true only if both true
`		`	OR
!	NOT	!(x > 5)	reverses the result
🔀 (4) Conditional Statements

Used to make decisions.

a) if, else if, else
let marks = 75;

if (marks > 90) {
  console.log("Excellent");
} else if (marks > 60) {
  console.log("Good");
} else {
  console.log("Needs improvement");
}

b) switch

Used when you have many options.

let color = "red";

switch(color) {
  case "red":
    console.log("Stop");
    break;
  case "green":
    console.log("Go");
    break;
  default:
    console.log("Invalid color");
}

🔁 (5) Loops

Loops repeat actions automatically.

a) for loop
for (let i = 1; i <= 5; i++) {
  console.log(i);
}

b) while loop
let i = 1;
while (i <= 5) {
  console.log(i);
  i++;
}

c) do-while loop

Runs at least once:

let i = 1;
do {
  console.log(i);
  i++;
} while (i <= 5);

🧩 (6) Functions

Functions are reusable blocks of code.

a) Function declaration
function greet() {
  console.log("Hello!");
}
greet();

b) Function expression
const greet = function() {
  console.log("Hello!");
};
greet();

c) Arrow function

Modern, shorter syntax:

const greet = () => {
  console.log("Hello!");
};
greet();

💬 (7) Template literals

Used to insert variables easily inside text using backticks (`).

Example:

let name = "Siva";
console.log(`Hello ${name}!`); // Hello Siva!

✍️ (8) Comments in JS

Comments are notes for yourself — the computer ignores them.

Single line:

// This is a single-line comment


Multi-line:

/* 
  This is a
  multi-line comment
*/

🪲 (9) Debugging

To find and fix errors.

a) console.log()

Shows messages or variable values:

let x = 10;
console.log(x);

b) debugger

Pauses the program to inspect values (used in browsers):

let x = 10;
debugger; // pauses execution here
console.log(x);

🧠 (10) JS Best Practices
Practice	Why it’s important
Avoid global variables	Prevents naming conflicts and bugs
Use strict mode ('use strict';)	Helps catch mistakes (like undeclared variables)
Use let and const	Safer and modern than var
Keep code readable	Use clear variable names
Test often with console.log()	Easier debugging

Example:

'use strict';
let name = "Siva";
console.log(name);




===============================> Level 3 — JavaScript Arrays


🧱 (1) Create Arrays

An array is like a box that can hold multiple values under one name.

Example:

let arr = [1, 2, 3];


Here:

arr[0] → first element (1)

arr[1] → second element (2)

arr[2] → third element (3)

You can store anything inside — numbers, strings, even other arrays:

let fruits = ["apple", "banana", "mango"];

🔍 (2) Access Elements

You access array items using index numbers (starting from 0).

let fruits = ["apple", "banana", "mango"];
console.log(fruits[0]); // apple
console.log(fruits[1]); // banana

✏️ (3) Modify Elements

You can change a value by referring to its index.

let arr = [1, 2, 3];
arr[1] = 10;
console.log(arr); // [1, 10, 3]

🧰 (4) Array Methods

These are built-in tools that let you easily add, remove, or search items.

a) Add / Remove Elements
Method	Action	Example	Result
push()	Add to end	arr.push(4)	[1,2,3,4]
pop()	Remove last	arr.pop()	[1,2]
shift()	Remove first	arr.shift()	[2,3]
unshift()	Add to beginning	arr.unshift(0)	[0,1,2,3]

Example:

let arr = [1, 2, 3];
arr.push(4);     // [1, 2, 3, 4]
arr.pop();       // [1, 2, 3]
arr.unshift(0);  // [0, 1, 2, 3]
arr.shift();     // [1, 2, 3]

b) Search in Array
Method	Description	Example	Result
indexOf()	Gives the position	arr.indexOf(2)	1
includes()	Checks if present	arr.includes(2)	true

Example:

let arr = [1, 2, 3];
console.log(arr.indexOf(3));  // 2
console.log(arr.includes(4)); // false

🔁 (5) Iteration — Looping through arrays

These methods help you go through every item in an array.

a) forEach() → Just do something for each item
let arr = [1, 2, 3];
arr.forEach(num => console.log(num));
// prints: 1 2 3

b) map() → Creates a new array by transforming each item
let arr = [1, 2, 3];
let doubled = arr.map(num => num * 2);
console.log(doubled); // [2, 4, 6]

c) filter() → Creates a new array with items that pass a condition
let arr = [1, 2, 3, 4, 5];
let even = arr.filter(num => num % 2 === 0);
console.log(even); // [2, 4]

d) reduce() → Combines all items into one value (like total sum)
let arr = [1, 2, 3, 4];
let sum = arr.reduce((total, num) => total + num, 0);
console.log(sum); // 10

🧩 (6) Multi-Dimensional Arrays

Arrays inside arrays — useful for rows and columns (like a table).

Example:

let matrix = [
  [1, 2, 3],
  [4, 5, 6]
];
console.log(matrix[0][1]); // 2
console.log(matrix[1][2]); // 6

🌈 (7) Spread Operator (...)

Used to copy or merge arrays easily.

let arr = [1, 2, 3];
let arr2 = [...arr];  // copy
console.log(arr2); // [1, 2, 3]


Also used to join arrays:

let a = [1, 2];
let b = [3, 4];
let combined = [...a, ...b];
console.log(combined); // [1, 2, 3, 4]

🧩 (8) Destructuring Arrays

Extract values from an array into separate variables easily.

let arr = [10, 20, 30];
let [a, b] = arr;
console.log(a); // 10
console.log(b); // 20


You can also skip items:

let [x, , z] = [1, 2, 3];
console.log(x, z); // 1, 3

🔃 (9) Sorting & Reversing Arrays
let arr = [3, 1, 4, 2];
arr.sort();    // [1, 2, 3, 4]
arr.reverse(); // [4, 3, 2, 1]


⚠️ Note: sort() works alphabetically by default.
If you want to sort numbers correctly, use:

arr.sort((a, b) => a - b);

🔡 (10) Convert Array to String

join() combines all elements into a string.

let arr = ["apple", "banana", "mango"];
let str = arr.join(",");
console.log(str); // "apple,banana,mango"



===============================> Level 4 — JavaScript Objects


🧱 (1) Create Objects

An object is like a real-world item — it has properties (details) and values.

Example:

let person = { name: "John", age: 30 };


Think of it like this:
🧍 John → has a name (“John”) and age (30).

🔍 (2) Access Properties

You can read values in two ways:

a) Dot notation
console.log(person.name); // John

b) Bracket notation
console.log(person["age"]); // 30


Bracket notation is useful when property names come from variables or have spaces.

✏️ (3) Modify Properties

You can change a value easily:

person.age = 31;
console.log(person.age); // 31

➕ (4) Add New Properties

You can add new details anytime:

person.city = "Hyderabad";
console.log(person); // {name: "John", age: 31, city: "Hyderabad"}

❌ (5) Delete Properties

You can remove a property:

delete person.name;
console.log(person); // {age: 31, city: "Hyderabad"}

🧰 (6) Object Methods

These are built-in functions that work with objects.

a) Object.keys(obj) → Gives all property names
let keys = Object.keys(person);
console.log(keys); // ["age", "city"]

b) Object.values(obj) → Gives all property values
let values = Object.values(person);
console.log(values); // [31, "Hyderabad"]

c) Object.entries(obj) → Gives key-value pairs
let entries = Object.entries(person);
console.log(entries); // [["age",31], ["city","Hyderabad"]]

🏗️ (7) Nested Objects & Arrays

Objects can contain other objects or arrays — like layers of information.

Example:

let student = {
  name: "Siva",
  age: 25,
  address: {
    city: "Chennai",
    pin: 600001
  },
  subjects: ["Math", "Science"]
};

console.log(student.address.city);  // Chennai
console.log(student.subjects[0]);   // Math

✂️ (8) Destructuring Objects

Extract values quickly from objects.

Example:

let person = { name: "John", age: 30 };
let { name, age } = person;

console.log(name); // John
console.log(age);  // 30


You can also rename:

let { name: fullName } = person;
console.log(fullName); // John

🌈 (9) Spread & Rest Operators (with Objects)
🧩 Spread → Used to copy or merge objects
let person = { name: "John", age: 30 };
let updatedPerson = { ...person, city: "Hyderabad" };
console.log(updatedPerson); // {name: "John", age: 30, city: "Hyderabad"}

🧺 Rest → Used to collect remaining properties
let { name, ...rest } = updatedPerson;
console.log(name); // John
console.log(rest); // {age: 30, city: "Hyderabad"}

🔁 (10) Loop Through Objects

You can loop (iterate) through object properties.

a) for...in → Loops through keys
let person = { name: "John", age: 30, city: "Hyderabad" };

for (let key in person) {
  console.log(key, ":", person[key]);
}

// Output:
// name : John
// age : 30
// city : Hyderabad

b) for...of with Object.entries()
for (let [key, value] of Object.entries(person)) {
  console.log(`${key}: ${value}`);
}

// Output:
// name: John
// age: 30
// city: Hyderabad




===============================> Level 5 — JavaScript Functions & Scope


🧩 (1) Function Declaration vs Expression

A function is like a mini program inside your program — it does a specific job.

🧱 Function Declaration

This is the normal way to define a function.

function greet() {
  console.log("Hello!");
}
greet(); // Hello!


✅ You can call it before or after it’s written.

⚙️ Function Expression

Here, you store a function inside a variable.

const greet = function() {
  console.log("Hello!");
};
greet(); // Hello!


⚠️ You cannot call it before it’s defined (since it’s stored in a variable).

⚡ (2) Arrow Functions & this

Arrow functions are a shorter and modern way to write functions.

const greet = () => {
  console.log("Hello!");
};

🧠 this difference

In normal functions, this can change depending on how the function is called.

In arrow functions, this is fixed — it takes the value from where it was created.

Example:

const person = {
  name: "Siva",
  greet: function() {
    console.log("Hi, " + this.name);
  }
};
person.greet(); // Hi, Siva


If we used an arrow function inside greet, this might not refer to the person object — that’s why understanding this is important later when you learn classes.

🧮 (3) Parameters & Arguments

Parameters = variable names in the function definition.

Arguments = actual values you pass when calling it.

Example:

function add(a, b) {   // a, b → parameters
  console.log(a + b);
}
add(5, 10);             // 5, 10 → arguments

🧱 (4) Default Parameters

You can give a default value if no argument is passed.

function greet(name = "Guest") {
  console.log("Hello " + name);
}
greet();          // Hello Guest
greet("Siva");    // Hello Siva

🔢 (5) Rest Parameters

Used when you don’t know how many arguments will come.
It collects them all into an array (... is called the rest operator).

function sum(...nums) {
  console.log(nums); // [1, 2, 3, 4]
  return nums.reduce((total, n) => total + n, 0);
}
console.log(sum(1, 2, 3, 4)); // 10

🎁 (6) Return Values from Functions

Functions can return results instead of just printing.

function add(a, b) {
  return a + b;
}

let result = add(5, 10);
console.log(result); // 15


Tip: return stops the function immediately.

🧱 (7) Function Scope & Block Scope

Scope means “where a variable is visible.”

function demo() {
  let x = 10; // only visible inside the function
  console.log(x);
}
demo();
// console.log(x); ❌ Error — x not defined outside


Block scope works for let and const inside { }.

{
  let y = 20;
}
// console.log(y); ❌ Error

🌍 (8) Global vs Local Variables
Type	Where it’s visible	Example
Global	Everywhere in code	let name = "Siva";
Local	Only inside function	function test(){ let x=10; }

Example:

let message = "Hello"; // Global

function sayHi() {
  let name = "Siva"; // Local
  console.log(message + " " + name);
}

sayHi(); // Hello Siva
// console.log(name); ❌ Error (local variable)

🧠 (9) Closures

A closure happens when a function remembers variables from its outer function, even after that outer function has finished running.

Example:

function outer() {
  let count = 0;
  return function inner() {
    count++;
    console.log(count);
  };
}

const counter = outer();
counter(); // 1
counter(); // 2
counter(); // 3


Here, inner() still remembers count even after outer() has completed — that’s a closure.
(Think of it like a backpack that carries the outer variable with it.)

⚙️ (10) IIFE (Immediately Invoked Function Expression)

A function that runs immediately after it’s created.

(function() {
  console.log("Runs instantly!");
})();


✅ Used to create temporary private code areas (so variables don’t mix with others).





===============================> Level 6 — JavaScript DOM Manipulation


(1) Select elements
a) document.getElementById()

👉 Finds an element using its id.

<p id="demo">Hello</p>

let para = document.getElementById("demo");
console.log(para.innerText);


✅ Output: Hello

b) document.querySelector()

👉 Finds the first matching element (like CSS selector).

<p class="text">One</p>
<p class="text">Two</p>

let first = document.querySelector(".text");
console.log(first.innerText);


✅ Output: One

c) document.querySelectorAll()

👉 Finds all matching elements and gives a list.

let all = document.querySelectorAll(".text");
console.log(all[1].innerText);


✅ Output: Two

(2) Modify content
element.innerText

👉 Changes only visible text.

para.innerText = "Welcome!";


✅ Changes: <p>Hello</p> → <p>Welcome!</p>

element.innerHTML

👉 Changes HTML structure inside.

para.innerHTML = "<b>Welcome!</b>";


✅ Now text appears bold.

(3) Modify attributes
element.setAttribute()

👉 Add or change an attribute.

img.setAttribute("src", "new.jpg");


✅ Changes image source.

element.getAttribute()

👉 Read the current value of an attribute.

let link = document.getElementById("myLink");
console.log(link.getAttribute("href"));


✅ Output: current link URL (like https://google.com)

(4) Change CSS styles dynamically

👉 You can directly change style using .style

element.style.color = "red";
element.style.backgroundColor = "yellow";


✅ Changes the element’s color and background instantly.

(5) Add / Remove / Toggle classes

👉 Used to control CSS classes dynamically.

element.classList.add("active");      // Adds a class
element.classList.remove("hidden");   // Removes a class
element.classList.toggle("dark");     // Adds if missing, removes if present


✅ Helps you control styling easily (for dark mode, highlights, etc.)

(6) Create & Append elements

👉 Create a new HTML element and put it inside another.

let newDiv = document.createElement("div");
newDiv.innerText = "I’m new!";
document.body.appendChild(newDiv);


✅ A new <div> appears on the webpage.

(7) Remove elements from DOM

👉 Delete an element completely.

element.remove();


✅ That element disappears from the page.

(8) Event listeners

👉 Let JS “listen” to user actions like click, hover, typing, etc.

button.addEventListener("click", function() {
  alert("Button clicked!");
});


✅ Shows alert when you click the button.

(9) Event delegation

👉 Instead of adding click events to every small item, listen on their parent.

document.getElementById("list").addEventListener("click", (e) => {
  if (e.target.tagName === "LI") {
    alert("You clicked: " + e.target.innerText);
  }
});


✅ Works for all list items — even new ones added later.

(10) Form input handling

👉 Read or control user input.

<input id="username" type="text" value="John">

let name = document.getElementById("username").value;
console.log(name);


✅ Output: John





===============================> Level 7 — JavaScript Events & Timers


(1) 🖱️ Mouse Events

These happen when you use your mouse.

button.addEventListener("click", () => console.log("Button clicked"));
button.addEventListener("mouseover", () => console.log("Mouse over"));
button.addEventListener("mouseout", () => console.log("Mouse out"));


✅ Example:

click → when you click

mouseover → when you move the mouse over an element

mouseout → when you move the mouse away

(2) ⌨️ Keyboard Events
document.addEventListener("keydown", () => console.log("Key pressed down"));
document.addEventListener("keyup", () => console.log("Key released"));
document.addEventListener("keypress", () => console.log("Key pressed"));


✅ Example:
When you type something, JavaScript can detect which key you pressed.

(3) 🧠 Event Object Properties

Every event has a special object (usually called event or e) that gives details about the action.

button.addEventListener("click", (event) => {
  console.log(event.target); // Which element was clicked
  console.log(event.type);   // Type of event (e.g., "click")
});


✅ Example: Helps to know what triggered the event.

(4) 🚫 Prevent Default & Stop Propagation
a) event.preventDefault()

👉 Stops the browser’s default action.

form.addEventListener("submit", (e) => {
  e.preventDefault(); // Stops page refresh
  console.log("Form handled manually!");
});

b) event.stopPropagation()

👉 Stops the event from bubbling up to parent elements.

child.addEventListener("click", (e) => {
  e.stopPropagation();
  console.log("Child clicked only!");
});


✅ Example: Useful when multiple elements have click events.

(5) 🧾 Form Events
form.addEventListener("submit", (e) => console.log("Form submitted"));
input.addEventListener("change", () => console.log("Value changed"));
input.addEventListener("input", () => console.log("Typing..."));


✅ Example:

submit → when form is submitted

change → when value changes (after blur)

input → while typing

(6) ⏰ setTimeout & clearTimeout

👉 Run code once after a delay.

let timer = setTimeout(() => console.log("Hello after 2 seconds"), 2000);
clearTimeout(timer); // Cancels it before it runs


✅ Example: Used for delays or showing messages after few seconds.

(7) ⏱️ setInterval & clearInterval

👉 Run code repeatedly every given time.

let count = 0;
let interval = setInterval(() => {
  count++;
  console.log("Count:", count);
  if (count === 5) clearInterval(interval); // Stop after 5 times
}, 1000);


✅ Example: Used for clocks, timers, etc.

(8) ⚡ Debouncing Events

👉 Waits for a pause before running code (avoids too many calls).

Example: Run function only after typing stops.

let timer;
input.addEventListener("input", () => {
  clearTimeout(timer);
  timer = setTimeout(() => console.log("Stopped typing!"), 500);
});


✅ Useful for search boxes or filters.

(9) 🚀 Throttling Events

👉 Runs code at fixed intervals, even if events happen fast.

let lastTime = 0;
window.addEventListener("scroll", () => {
  let now = Date.now();
  if (now - lastTime > 1000) {
    console.log("Scrolling...");
    lastTime = now;
  }
});


✅ Useful for scroll or resize events.

(10) 🎉 Custom Events

👉 You can create and trigger your own events.

let myEvent = new CustomEvent("greet", { detail: { name: "John" } });

document.addEventListener("greet", (e) => {
  console.log("Hello", e.detail.name);
});

document.dispatchEvent(myEvent);


✅ Output: Hello John



===============================> Level 8 — JavaScript ES6+ Features


(1) 🧱 let & const

Used to declare variables (modern replacement for var).

let name = "John";   // can change
name = "David";

const age = 25;      // cannot change
// age = 30 ❌ Error


✅ let → changeable
✅ const → fixed (constant)

(2) ⚡ Arrow Functions

A shorter way to write functions.

// Normal function
function sayHello() {
  console.log("Hello!");
}

// Arrow function
const sayHi = () => console.log("Hi!");


✅ Uses less code
✅ Automatically binds this (good for callbacks and events)

(3) 💬 Template Literals

Used for cleaner strings with variables inside backticks `, not quotes.

let name = "John";
console.log(`Hello ${name}, welcome!`);


✅ Easier string building than "Hello " + name + "!"

(4) ⚙️ Default Parameters

If no argument is passed, use the default value.

function greet(name = "Guest") {
  console.log(`Hello, ${name}`);
}

greet();       // Hello, Guest
greet("Ravi"); // Hello, Ravi

(5) 📦 Destructuring Arrays & Objects

Extract values easily.

From arrays:
let arr = [1, 2, 3];
let [a, b] = arr;
console.log(a, b); // 1 2

From objects:
let user = {name: "John", age: 30};
let {name, age} = user;
console.log(name, age); // John 30


✅ Quick unpacking of values.

(6) 🌈 Spread & Rest Operators (...)

Same symbol but used differently.

Spread → expand things
let arr1 = [1, 2];
let arr2 = [...arr1, 3, 4];
console.log(arr2); // [1,2,3,4]

Rest → collect multiple values
function sum(...nums) {
  console.log(nums);
}
sum(1, 2, 3); // [1, 2, 3]

(7) 📦 Modules: import & export

Used to split code into multiple files.

file1.js

export const name = "John";
export function sayHi() { console.log("Hi!"); }


file2.js

import { name, sayHi } from "./file1.js";
sayHi(); // Hi!


✅ Helps organize large projects.

(8) 👨‍🏫 Classes & Inheritance

Used to create reusable blueprints for objects.

class Person {
  constructor(name) {
    this.name = name;
  }
  greet() {
    console.log(`Hello, I'm ${this.name}`);
  }
}

class Employee extends Person {
  constructor(name, role) {
    super(name);
    this.role = role;
  }
  work() {
    console.log(`${this.name} is working as ${this.role}`);
  }
}

let emp = new Employee("John", "Developer");
emp.greet(); // Hello, I'm John
emp.work();  // John is working as Developer


✅ extends → means the child inherits from the parent.

(9) 🗺️ Map, Set, WeakMap, WeakSet
Map → stores key-value pairs
let map = new Map();
map.set("name", "John");
console.log(map.get("name")); // John

Set → stores unique values only
let set = new Set([1, 2, 2, 3]);
console.log(set); // {1, 2, 3}

WeakMap / WeakSet → same as Map/Set but for objects only (used rarely for memory-safe code).
(10) ❓ Optional Chaining (?.)

Safely access deep properties without error.

let user = { profile: { name: "John" } };
console.log(user.profile?.name); // John
console.log(user.address?.city); // undefined (no error)


✅ Prevents “Cannot read property of undefined” errors.



===============================> Level 9 — JavaScript Asynchronous Programming