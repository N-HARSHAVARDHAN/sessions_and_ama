
### 1. Difference between `makemigrations` and `migrate` in Django

**makemigrations**

* Creates migration files based on changes made in models.
* Does not change the database.

**Command:**

```bash
python manage.py makemigrations
```

**migrate**

* Applies migration files to the database.
* Updates the database schema.

**Command:**

```bash
python manage.py migrate
```

---

### 2. Why is Django a Framework and not a Library?

A **library** provides specific functionality and is called by your code.

A **framework** provides the overall structure and calls your code when needed.

Django follows the **Inversion of Control** principle, where Django controls the application flow, making it a framework.

---

### 3. What does `render()` do in Django?

`render()` combines a template with data and returns an HTTP response.

**Example:**

```python
return render(request, 'index.html', {'name': 'Harsha'})
```

It loads the template, fills in the data, and sends the HTML page to the browser.

---

### 4. Difference between Aggregation and Annotation

**Aggregation**

* Calculates a value for the entire queryset.
* Returns a dictionary.

```python
Book.objects.aggregate(Avg('price'))
```

**Annotation**

* Calculates a value for each object.
* Adds a new field to every record.

```python
Author.objects.annotate(num_books=Count('book'))
```

---

### 5. What does an empty string URL (`''`) signify?

An empty string URL represents the **root URL** of an application.

```python
path('', views.home, name='home')
```

When a user visits the app's base URL, this view is executed.

---

### 6. What is `MANIFEST.in` used for?

`MANIFEST.in` specifies additional files to include when creating a Python package.

Examples:

* Templates
* Static files
* Documentation

Example:

```text
include README.md
recursive-include templates *
```

---

### 7. What is a View in Django?

A view is a Python function or class that receives a request and returns a response.

Example:

```python
def home(request):
    return HttpResponse("Hello World")
```

Views contain the application's business logic.

---

### 8. What is the use of `manage.py`?

`manage.py` is Django's command-line utility.

Used for:

* Running the server
* Creating migrations
* Applying migrations
* Creating superusers
* Running tests

Examples:

```bash
python manage.py runserver
python manage.py migrate
```

---

### 9. Command for using shell for SQL operations in Django

Open Django shell:

```bash
python manage.py shell
```

Open database shell directly:

```bash
python manage.py dbshell
```

`dbshell` allows executing SQL queries directly on the database.

---

### 10. Use of `{% load static %}`

Loads Django's static file template tag.

```html
{% load static %}
<img src="{% static 'images/logo.png' %}">
```

Used to access CSS, JavaScript, and image files.

---

### 11. How do you define a One-to-Many relationship?

Using `ForeignKey`.

Example:

```python
class Author(models.Model):
    name = models.CharField(max_length=100)

class Book(models.Model):
    title = models.CharField(max_length=100)
    author = models.ForeignKey(
        Author,
        on_delete=models.CASCADE
    )
```

One Author can have many Books.

---

### 12. What does `redirect()` do in Django?

`redirect()` sends the user to another URL.

Example:

```python
from django.shortcuts import redirect

return redirect('home')
```

The browser is redirected to the specified page.

---

### 13. How to register models in Admin?

In `admin.py`:

```python
from django.contrib import admin
from .models import Book

admin.site.register(Book)
```

This makes the model available in the Django Admin panel.

---

### 14. Where is project configuration stored?

Project configuration is mainly stored in:

```text
project_name/settings.py
```

Contains:

* Installed apps
* Database settings
* Middleware
* Templates
* Static files
* Security settings

It is the central configuration file of a Django project.
