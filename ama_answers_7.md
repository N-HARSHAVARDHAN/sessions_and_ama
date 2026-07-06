# AMA Questions and answers:

### 1. What is `re_path()`?

`re_path()` is used in Django `urls.py` to create URL patterns using **regular expressions (regex)**. It is useful when you need complex URL matching. For simple URLs, `path()` is preferred.

---

### 2. What is the `@shared_task` decorator used for in Celery?

`@shared_task` is used to create **background tasks** in Celery without directly importing the Celery app. It is commonly used for sending emails, processing files, and running long tasks asynchronously.

---

### 3. What are HTTP Methods?

HTTP methods define the action a client wants to perform on the server.

* **GET** – Retrieve data
* **POST** – Create new data
* **PUT** – Update entire data
* **PATCH** – Update part of the data
* **DELETE** – Delete data

---

### 4. API endpoint starts with which URL?

There is no fixed URL, but in Django REST Framework APIs usually start with:

* `/api/`
* `/api/v1/`
* `/api/v2/`

Example:

```
http://127.0.0.1:8000/api/v1/students/
```

---

### 5. What is `autodiscover_tasks()` in Celery?

`autodiscover_tasks()` automatically searches all installed Django apps for a `tasks.py` file and registers the Celery tasks, so you don't need to import them manually.

---

### 6. What is a Decorator?

A decorator is a Python feature that **adds extra functionality to a function or class without modifying its original code**. In Django, decorators like `@login_required` are commonly used for authentication and permissions.

---

### 7. What does the `__init__.py` file do?

`__init__.py` tells Python that a directory is a **package**. It is executed when the package is imported and can also be used for package initialization, such as loading Celery.

---

### 8. What is the Priority of CSS Selectors?

CSS applies styles based on **specificity**. The priority is:

1. Inline CSS
2. ID Selector (`#id`)
3. Class Selector (`.class`)
4. Element Selector (`p`, `div`)
5. Universal Selector (`*`)

If two selectors have the same specificity, the one written last is applied.

---

### 9. Explain the Request and Response Cycle in Django.

The request-response cycle is the process Django follows to handle a user request:

1. Browser sends a request.
2. Django receives the request.
3. `urls.py` matches the URL.
4. The corresponding view is called.
5. The view interacts with the model/database if needed.
6. Django returns an HTML page or JSON response to the browser.

**Flow:**

```
Browser → URL → View → Model (Database) → Response → Browser
```
