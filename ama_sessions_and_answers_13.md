# Adhikya Edammala - What is Prompting?

**Answer:**
Prompting is the process of giving clear instructions or questions (called a **prompt**) to an AI model so it can generate the desired response.

A good prompt helps the AI understand exactly what you want, leading to more accurate and useful results.

**Example:**

```text
Prompt:
Explain React Hooks in simple English with an example.
```


---

# Allanki VV Manikanta Sai - Difference Between PUT and PATCH

| PUT                                         | PATCH                                       |
| ------------------------------------------- | ------------------------------------------- |
| Updates the entire resource.                | Updates only specific fields of a resource. |
| All fields are usually sent in the request. | Only the fields to be changed are sent.     |
| Missing fields may be overwritten.          | Unchanged fields remain the same.           |
| Used for full updates.                      | Used for partial updates.                   |

**Example:**

Suppose a user has:

```json
{
  "name": "John",
  "age": 25,
  "city": "Delhi"
}
```

**PUT Request**

```json
{
  "name": "John",
  "age": 26,
  "city": "Mumbai"
}
```

Entire object is replaced.

**PATCH Request**

```json
{
  "age": 26
}
```

Only the age is updated.


---

# Boorle Sowmya Sri Lakshmi - Difference Between XSS and CSRF

| XSS (Cross-Site Scripting)                                                            | CSRF (Cross-Site Request Forgery)                         |
| ------------------------------------------------------------------------------------- | --------------------------------------------------------- |
| Injects malicious JavaScript into a website.                                          | Tricks a logged-in user into performing unwanted actions. |
| Targets website users.                                                                | Exploits the user's authenticated session.                |
| Executes malicious scripts in the browser.                                            | Sends unauthorized requests without the user's knowledge. |
| Prevented using input validation, output escaping, and Content Security Policy (CSP). | Prevented using CSRF tokens and SameSite cookies.         |

### Example

**XSS**

```html
<script>alert("Hacked")</script>
```

If not sanitized, the script runs in another user's browser.

**CSRF**

A user is logged into a banking website. They visit a malicious website that secretly sends:

```http
POST /transfer-money
```

The bank processes it because the user's session cookie is automatically sent.


---

# Md Musharaf - What is a Message Broker?

**Answer:**
A message broker is software that allows different applications or services to communicate by sending and receiving messages asynchronously.

Instead of communicating directly, one service sends a message to the broker, and another service receives it later.

**Examples:**

* RabbitMQ
* Apache Kafka
* ActiveMQ
* Redis Streams

### Flow

```text
Producer → Message Broker → Consumer
```

**Benefits:**

* Decouples services
* Handles asynchronous communication
* Improves scalability
* Provides reliable message delivery


---

# Rongala Vasu - How to Convert an Object into an Array?

**Answer:**
JavaScript provides built-in methods to convert an object into an array.

### 1. Get Keys

```javascript
const user = {
  name: "John",
  age: 25
};

console.log(Object.keys(user));
```

Output:

```javascript
["name", "age"]
```

---

### 2. Get Values

```javascript
console.log(Object.values(user));
```

Output:

```javascript
["John", 25]
```

---

### 3. Get Key-Value Pairs

```javascript
console.log(Object.entries(user));
```

Output:

```javascript
[
  ["name", "John"],
  ["age", 25]
]
```


---

# Vikas Mehta - Different Life Cycle in React

**Answer:**
A React component goes through three main lifecycle phases.

## 1. Mounting

The component is created and added to the DOM.

Examples:

* Component is displayed for the first time.
* Data is fetched from an API.

```javascript
useEffect(() => {
  console.log("Component Mounted");
}, []);
```

---

## 2. Updating

The component re-renders when its **state** or **props** change.

Example:

```javascript
useEffect(() => {
  console.log("Component Updated");
}, [count]);
```

Whenever `count` changes, this effect runs.

---

## 3. Unmounting

The component is removed from the DOM.

Example:

```javascript
useEffect(() => {
  return () => {
    console.log("Component Unmounted");
  };
}, []);
```

This is commonly used to:

* Remove event listeners
* Clear timers
* Close WebSocket connections

---

### React Lifecycle Flow

```text
Mounting
    ↓
Updating (0 or many times)
    ↓
Unmounting
```
