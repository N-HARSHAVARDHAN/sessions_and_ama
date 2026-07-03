### 1. What is `values_list()` in Django ORM?

`values_list()` retrieves specific field values from a queryset instead of returning complete model objects.

```python
User.objects.values_list('username', flat=True)
```

---

### 2. What does `on_delete=models.CASCADE` do?

`models.CASCADE` automatically deletes all related child objects when the parent object is deleted.

```python
author = models.ForeignKey(Author, on_delete=models.CASCADE)
```

Deleting an `Author` also deletes its related `Book` objects.

---

### 3. What does `on_delete=models.PROTECT` do?

`models.PROTECT` prevents deletion of a parent object if related child objects exist.

```python
author = models.ForeignKey(Author, on_delete=models.PROTECT)
```

Trying to delete the `Author` raises a `ProtectedError`.

---

### 4. What are Serializers?

Serializers convert Django model instances into formats like JSON and validate incoming data before saving.

```python
class UserSerializer(serializers.ModelSerializer):
    class Meta:
        model = User
        fields = '__all__'
```

---

### 5. What is Redis?

Redis is an in-memory data store used for caching, session storage, and as a message broker for Celery.

**Example:**

* Cache frequently accessed data.
* Store Celery task queues.

---

### 6. How do you add a custom app in `settings.py`?

Add the app name to the `INSTALLED_APPS` list.

```python
INSTALLED_APPS = [
    ...
    'accounts',
]
```

---

### 7. Why do we use Signals in Django?

Signals allow code to run automatically when specific events (like saving or deleting a model) occur.

```python
@receiver(post_save, sender=User)
def create_profile(sender, instance, created, **kwargs):
    if created:
        Profile.objects.create(user=instance)
```

---

### 8. What is Pagination?

Pagination divides a large queryset into smaller pages to improve performance and user experience.

```python
from django.core.paginator import Paginator

paginator = Paginator(posts, 10)
```

Displays 10 records per page.

---

### 9. What is the `@property` decorator in Python?

The `@property` decorator lets you access a method like an attribute without using parentheses.

```python
class User:
    @property
    def full_name(self):
        return f"{self.first_name} {self.last_name}"
```

Usage:

```python
user.full_name
```

instead of:

```python
user.full_name()
```

---

### 10. What does `app.autodiscover_tasks()` do in Celery?

`app.autodiscover_tasks()` automatically discovers and registers `tasks.py` files from all installed Django apps.

```python
app.autodiscover_tasks()
```

You don't need to import each app's `tasks.py` manually.

---

### 11. Why do we use WhiteNoise Middleware?

WhiteNoise allows Django to serve static files (CSS, JavaScript, images) directly in production without requiring a separate web server like Nginx.

```python
MIDDLEWARE = [
    ...
    "whitenoise.middleware.WhiteNoiseMiddleware",
]
```

It simplifies deployment and improves static file handling.
