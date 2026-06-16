### 1. What is an HTMLCollection?

An **HTMLCollection** is an array-like collection of HTML elements returned by some DOM methods.

```js
const elements = document.getElementsByClassName("box");

console.log(elements);
```

Features:

* Array-like object
* Access elements using index
* Live collection (updates automatically when DOM changes)
* Does not support array methods directly

```js
console.log(elements[0]);
```

---

### 2. What are Ways to Get Elements Using DOM?

JavaScript provides multiple methods to select elements.

```js
document.getElementById("id");
```

```js
document.getElementsByClassName("class");
```

```js
document.getElementsByTagName("p");
```

```js
document.querySelector(".box");
```

```js
document.querySelectorAll(".box");
```

**querySelector()** returns the first match, while **querySelectorAll()** returns all matching elements.

---

### 3. How to Define Instance Method, Class Method and Static Method in Python?

**Instance Method**

Works with object instances.

```python
class Student:
    def show(self):
        print("Instance Method")
```

**Class Method**

Uses `@classmethod` and works with class data.

```python
class Student:
    @classmethod
    def display(cls):
        print("Class Method")
```

**Static Method**

Uses `@staticmethod` and doesn't depend on class or object data.

```python
class Student:
    @staticmethod
    def greet():
        print("Static Method")
```

| Method          | Access                        |
| --------------- | ----------------------------- |
| Instance Method | Object data                   |
| Class Method    | Class data                    |
| Static Method   | Neither object nor class data |

---

### 4. What are Different HTTP Methods?

HTTP methods define actions performed on resources.

| Method  | Purpose                |
| ------- | ---------------------- |
| GET     | Retrieve data          |
| POST    | Create data            |
| PUT     | Update entire resource |
| PATCH   | Partial update         |
| DELETE  | Remove data            |
| HEAD    | Headers only           |
| OPTIONS | Supported methods      |

Example:

```http
GET /users
```

```http
POST /users
```

```http
DELETE /users/1
```

---

### 5. What is Event Loop?

The **Event Loop** allows JavaScript to handle asynchronous operations while remaining single-threaded.

Execution order:

1. Call Stack
2. Microtask Queue
3. Callback Queue

```js
console.log("Start");

setTimeout(() => console.log("Timer"), 0);

console.log("End");
```

Output:

```js
Start
End
Timer
```

The Event Loop moves tasks from queues into the Call Stack when it becomes empty.

---

### 6. What is the Purpose of Symbol in JavaScript?

`Symbol` is a primitive data type used to create unique identifiers.

```js
const id1 = Symbol("id");
const id2 = Symbol("id");

console.log(id1 === id2);
```

Output:

```js
false
```

Uses:

* Unique object keys
* Prevent property name conflicts
* Internal object properties

```js
const id = Symbol("id");

const user = {
    name: "John",
    [id]: 101
};
```

---

### 7. Difference Between isFinite() and Number.isFinite()

| isFinite()                      | Number.isFinite()  |
| ------------------------------- | ------------------ |
| Converts values before checking | No type conversion |
| Less strict                     | More strict        |
| Older method                    | Recommended        |

```js
console.log(isFinite("100"));
```

Output:

```js
true
```

```js
console.log(Number.isFinite("100"));
```

Output:

```js
false
```

---

### 8. What is Parallelism in JavaScript?

**Parallelism** means executing multiple tasks simultaneously using multiple threads or processors.

JavaScript is single-threaded, but parallelism can be achieved using:

* Web Workers
* Worker Threads (Node.js)

```js
const worker = new Worker("worker.js");

worker.postMessage("Start");
```

Benefits:

* Better performance
* Heavy computations don't block UI
* Faster execution

---

### 9. Difference Between Promise.any() and Promise.success()

There is **no Promise.success() method** in JavaScript.

**Promise.any()**

* Returns the first fulfilled promise.
* Ignores rejected promises.

```js
Promise.any([
    Promise.reject("Error"),
    Promise.resolve("Success")
]).then(console.log);
```

Output:

```js
Success
```

If all promises fail, it throws an `AggregateError`.

---

### 10. What is Object.freeze()?

`Object.freeze()` prevents modification of an object.

```js
const user = {
    name: "John"
};

Object.freeze(user);

user.name = "Mike";

console.log(user.name);
```

Output:

```js
John
```

It prevents:

* Adding properties
* Updating properties
* Deleting properties

```js
delete user.name;
```

Will not work.

---

### 11. What is element.closest()?

`closest()` finds the nearest ancestor that matches a CSS selector.

```html
<div class="parent">
    <button id="btn">Click</button>
</div>
```

```js
const btn = document.getElementById("btn");

const parent = btn.closest(".parent");

console.log(parent);
```

Uses:

* Finding parent containers
* Event delegation
* DOM traversal

---

### 12. Is Multiple Inheritance Possible in JavaScript?

JavaScript does not support multiple inheritance directly.

Invalid:

```js
class A {}
class B {}

class C extends A, B {}
```

Alternative: Mixins

```js
const canEat = {
    eat() {
        console.log("Eating");
    }
};

const canWalk = {
    walk() {
        console.log("Walking");
    }
};

class Person {}

Object.assign(Person.prototype, canEat, canWalk);
```

JavaScript supports single inheritance, but mixins can provide similar behavior.

---

### 13. How to Change Style of an Element Using DOM?

Use the `style` property.

```js
const box = document.getElementById("box");

box.style.color = "red";
box.style.backgroundColor = "yellow";
```

You can also use CSS classes.

```js
box.classList.add("active");
```

```css
.active {
    color: red;
    background: yellow;
}
```

Using classes is usually preferred for maintainability.

---

### 14. Why Do We Use Postman?

**Postman** is an API testing tool used to send requests and inspect responses without writing frontend code.

Example:

```http
GET /users
```

Postman helps developers:

* Test APIs
* Debug API responses
* Check status codes
* Add headers and authentication
* Save request collections
* Automate API testing

Common methods supported:

```http
GET
POST
PUT
PATCH
DELETE
```

It makes API development and testing much faster.
