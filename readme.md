# Javascript Refresher

## What we will learn

    1. What is Javascript
    2. How to Run Javascript
    3. Javascript Data Types
    4. Javascript Variable
    5. Javascript Conditionals
    6. Javascript Loops
    7. Javascript Function
    8. Javascript Class (Object)

### What is Javascript

- Javascript is a high-level, dynamic programming languagae primarily used to create and control dynamic website.
- Anything that moves, changes, or updates on your screen without requiring you to manually refresh page.
- Is is one of the cre technologes of the World Wide Web, alongside HTML and CSS.

Roles of Javascript

- Build Interactive Websites
- Develop Singla Page Applications (React, Angular, Vue)
- Build Server-Side Applications (Node Js)
- Develop Progressive Web Apps (PWAs)
- Build Mobile Apps (React Native)
- Game Development
- Automate Tasks
- Data Visualization

### How to Run Javascript

Open your browser - Click right button on your mouse - Click on inspect - select console - write your code
On your pc - Download and install Node JS & Vs Code - Write code on Vs code - check terminal for output

### Javascript Data Types

Javascript has primarily 2 types of data

1. Primitive Data Types
   1. String
   2. Number
   3. Boolean
   4. Undefined
   5. Null
   6. Symbol
   7. BigInt
2. Non-Primitive,Complex or Object Data Types
   1. Object
   2. Array
   3. Function
   4. Date
   5. RegExp

Primitive মানে হচ্ছে সিঙ্গেল ডাটা। কোন ডাটা যদি আমাদেরকে সিঙ্গেল কোন ইনফরমেশন দেয় তবে সেটা হচ্ছে Primitive Data।
<br/>
যখন আমাদের গ্রুপ ডাটা নিয়ে কাজ করতে হবে তখন আমরা Non-Primitive ডাটা নিয়ে কাজ করব।

### Javascript Variable

variable হচ্ছে ডাটা কনটেইনার। কোন একটা ডাটাকে আমরা একটা নাম দিয়ে তার মধ্যে রাখি।

Javascript এ আমরা তিনভাবে variable ডিক্লেয়ার করতে পারি।

- var
- let
- const

2015 সালের পরে Javascript এ মেজর আপডেট আসে তার আগে আমরা variable ডিক্লেয়ার করতে var keyword টাই ব্যাবহার করতাম। কিন্তু এতে অনেক সমস্যা থাকায় এখন আর এটা তেমন ব্যবহৃত হয় না।

<br/>

2015 সালে Javascript let & const keyword আনে। এই let keyword দিয়ে কোন variable ডিক্লেয়ার করলে তাকে আবার re-assign করা যায়। কিন্ত const দিয়ে কোন variable ডিক্লেয়ার করলে তাকে আবার re-assign করা যায় না। কোন ডাটা পরিবর্তনযোগ্য হলে তাকে let দিয়ে এবং কোন ডাটা অপরিবর্তনযোগ্য হলে তাকে const দিয়ে ডিক্লেয়ার করতে হয়।

```
const  name      = "Raihan Gazi";

let age = 27;

```

আমরা আমাদের যেকোন টাইপের ডাটাকে আমাদের ভ্যারিয়েবলের মধ্যে রাখতে পারি।

```
const raihan = {
   name: "Raihan Gazi",
   age: 27
}

const fruits = ["Apple", "Orange", "Banana"];
```
