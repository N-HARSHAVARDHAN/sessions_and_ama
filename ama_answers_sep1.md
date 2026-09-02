# Ama Answers:

## 1. Adhikya Edammala — What is JWT?

A **JWT (JSON Web Token)** is a token used to securely transmit information between a client and a server, commonly for **authentication and authorization**.

After a user logs in, the server generates a JWT, and the client sends it with future requests.

**Example:**

```text
Client → Login → Server generates JWT

Client → Sends JWT with requests → Server verifies JWT
```

> **JWT = A token that proves the user's identity and permissions.**

---

## 2. Boorle Sowmya Sri Lakshmi — What is Meant by Persistent Queue and Persistent Message?

A **persistent queue** is a queue that is configured to survive even if the message broker restarts.

A **persistent message** is a message that is stored so it can survive a broker restart.

### Simple Difference

> **Persistent Queue = Queue survives restart**
> **Persistent Message = Message survives restart**

Both are commonly used in message brokers such as RabbitMQ to reduce the risk of losing important messages.

---

## 3. Md Musharaf — What is the Event Loop in JavaScript?

The **event loop** is a mechanism that allows JavaScript to handle **asynchronous operations** without blocking the main thread.

JavaScript is single-threaded, but operations such as API calls, timers, and file operations can be handled asynchronously.

### Example

```text
Call Stack → Executes JavaScript code

Web APIs → Handles async operations

Callback Queue → Stores completed callbacks

Event Loop → Moves callbacks to the Call Stack when it is free
```

> **Event Loop = The mechanism that helps JavaScript handle asynchronous tasks.**

---

## 4. Rongala Vasu — Which One is Stateless, JWT or Session?

**JWT is stateless**, while **traditional sessions are stateful**.

With JWT, the server usually does not need to store user session information.

With sessions, the server stores session information and identifies the user using a session ID.

> **JWT = Stateless**
> **Session = Stateful**

---

## 5. Vikas Mehta — What is a Bearer Token?

A **Bearer Token** is an access token sent with an API request to prove that the user is authorized to access a resource.

It is usually sent in the HTTP `Authorization` header.

```text
Authorization: Bearer <token>
```

> **Bearer Token = A token used to access protected resources.**
