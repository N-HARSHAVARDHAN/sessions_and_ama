# AMA ANSWERS:

## 1. Adhikya Edammala — What are Actions in Redux?

**Actions** are objects in Redux that describe **what happened** or what change should be made to the state.

An action usually contains a `type` property.

**Example:**

```js
{
  type: "INCREMENT"
}
```

> **Action = An object that describes what should happen to the state.**

---

## 2. Boorle Sowmya Sri Lakshmi — Difference Between Authentication and Authorization?

**Authentication** verifies **who the user is**.

**Authorization** determines **what the user is allowed to access**.

### Simple Difference

> **Authentication = Who are you?**
> **Authorization = What are you allowed to do?**

**Example:** Logging in with a username and password is authentication, while checking whether you can access an admin page is authorization.

---

## 3. Md Musharaf — What is `useDispatch`?

**`useDispatch`** is a React-Redux hook used to **send (dispatch) actions to the Redux store**.

**Example:**

```js
const dispatch = useDispatch();

dispatch({ type: "INCREMENT" });
```

> **useDispatch = Used to send actions to the Redux store.**

---

## 4. Rongala Vasu — What is a Slice in Redux?

A **slice** is a section of the Redux store that manages a **specific part of the application's state**, along with its reducers and actions.

**Example:**

```text
Redux Store
 ├── userSlice
 ├── cartSlice
 └── productSlice
```

> **Slice = A feature-specific part of Redux state and its related logic.**

---

## 5. Vikas Mehta — What are ORMs?

**ORM (Object-Relational Mapping)** is a technique that allows developers to interact with a database using **programming language objects instead of writing SQL queries directly**.

**Examples:** Sequelize, Prisma, and SQLAlchemy.

> **ORM = A tool that connects programming language objects with database tables.**
