
# 1. What is the Spread Operator (`...`)?

The spread operator expands elements of an array or properties of an object.

**Example:**

```javascript
const arr = [1, 2];
const newArr = [...arr, 3];
```

---

# 2. What is Temporal Dead Zone (TDZ)?

The Temporal Dead Zone is the period between entering a scope and the declaration of a `let` or `const` variable. Accessing it during this period causes an error.


---

# 3. Are Functions Hoisted?

Yes, function declarations are fully hoisted and can be called before their declaration.

**Example:**

```javascript
greet();

function greet() {
  console.log("Hello");
}
```

---

# 4. What is a Closure?

A closure is a function that can access variables from its outer scope even after the outer function has finished executing.

**Example:**

```javascript
function outer() {
  let count = 0;
  return function() {
    count++;
    return count;
  };
}
```

---

# 5. What is Object Cloning?

Object cloning means creating a copy of an object.

**Example:**

```javascript
const copy = { ...original };
```

---

# 6. Difference Between `exports` and `module.exports`

### exports

A shortcut reference to `module.exports`.

### module.exports

The actual object that gets exported from the module.

**Example:**

```javascript
module.exports = {
  name: "Harsha"
};
```

---

# 7. What is Hoisting?

Hoisting is JavaScript's behavior of moving declarations to the top of their scope before execution.

**Example:**

```javascript
console.log(a); // undefined
var a = 10;
```

---

# 8. What are Ways We Can Iterate Over Objects?

* `for...in`
* `Object.keys()`
* `Object.values()`
* `Object.entries()`

**Example:**

```javascript
for (let key in obj) {
  console.log(key);
}
```

---

# 9. What is an IIFE?

IIFE (Immediately Invoked Function Expression) is a function that executes immediately after it is created.

**Example:**

```javascript
(function() {
  console.log("Executed");
})();
```

---

# 10. How Can We Add Data Into an Object?

Using dot notation or bracket notation.

**Example:**

```javascript
user.name = "Harsha";
user["age"] = 22;
```

---

# 11. Difference Between `for...in` and `for...of`

### for...in

Iterates over keys or indexes.

### for...of

Iterates over values.

**Example:**

```javascript
for (let i in arr) {}   // indexes
for (let value of arr) {} // values
```

---

# 12. Difference Between Pass By Value and Pass By Reference

### Pass By Value

A copy of the value is passed.

### Pass By Reference

A reference to the object is copied.

**Example:**

```javascript
let a = 10;
let b = a;
```

```javascript
const obj2 = obj1;
```

---

# 13. What Does `setTimeout()` Do?

`setTimeout()` schedules a function to execute after a specified delay.

**Example:**

```javascript
setTimeout(() => {
  console.log("Hello");
}, 2000);
```

---

# 14. What Do You Mean by Error-First Callback?

In Node.js, the first parameter of a callback is reserved for errors and the second for the result.

**Example:**

```javascript
fs.readFile("file.txt", (err, data) => {
  if (err) return console.log(err);
  console.log(data);
});
```

---

# 15. There Are Many Backend Languages, Then Why Use JavaScript with Frontend?

* Same language on frontend and backend.
* Easier development and maintenance.
* Large ecosystem through Node.js and npm.
* Code can be shared between client and server.

