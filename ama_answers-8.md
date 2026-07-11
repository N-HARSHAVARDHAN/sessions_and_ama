# AMA Questions and Answers:

## 1. Adhikya Edammala: Some famous applications using Python

**Answer:**
Python is used by many popular applications, including:

* Instagram
* YouTube
* Dropbox
* Spotify
* Reddit
* Netflix
* Pinterest

Python is popular because it's easy to learn, scalable, and has a rich ecosystem of libraries.

---

## 2. Allanki VV Manikanta Sai: Some famous applications using Django

**Answer:**
Some well-known applications that use Django are:

* Instagram
* Pinterest
* Disqus
* Mozilla
* Bitbucket
* The Washington Post

Django is popular because it enables fast, secure, and scalable web development.

---

## 3. Arpit Yadav: What is a Dockerfile?

**Answer:**
A **Dockerfile** is a text file that contains instructions to automatically build a Docker image.

Example:

```dockerfile
FROM python:3.12
COPY . /app
WORKDIR /app
RUN pip install -r requirements.txt
CMD ["python", "manage.py", "runserver"]
```

---

## 4. Boorle Sowmya Sri Lakshmi: Difference between `required=True` and `required=False` in RabbitMQ

**Answer:**
There is **no `required=True` or `required=False` in RabbitMQ**.

If the interviewer meant **Django REST Framework**:

* `required=True` → Field is mandatory.
* `required=False` → Field is optional.

Example:

```python
name = serializers.CharField(required=True)
bio = serializers.CharField(required=False)
```

---

## 5. Md Musharaf: Difference between Docker Image and Docker Container

**Answer:**

| Docker Image              | Docker Container     |
| ------------------------- | -------------------- |
| Blueprint/template        | Running instance     |
| Immutable                 | Mutable              |
| Used to create containers | Runs the application |

Example:

```bash
docker build -t myapp .
docker run myapp
```

---

## 6. Naman Sharma: Default port of RabbitMQ

**Answer:**

* **5672** → AMQP (Application connection)
* **15672** → Management UI

Management UI:

```
http://localhost:15672
```

---

## 7. Parlapalli Sulochana: Difference between Deep Copy and `=` Operator

**Answer:**

| `=` Operator          | Deep Copy                        |
| --------------------- | -------------------------------- |
| Same object reference | Creates a new independent object |
| Changes affect both   | Changes don't affect the copy    |

Example:

```python
import copy

a = [1, 2]
b = a
c = copy.deepcopy(a)
```

---

## 8. Rongala Vasu: What is the use of Docker Engine?

**Answer:**
Docker Engine is the core component of Docker that:

* Builds Docker images
* Runs containers
* Manages images, networks, and volumes

Example:

```bash
docker run nginx
docker ps
```

---

## 9. Rovinpal Udupi: Difference between Exchange and Queue

**Answer:**

| Exchange                         | Queue                          |
| -------------------------------- | ------------------------------ |
| Routes messages                  | Stores messages                |
| Receives messages from producers | Delivers messages to consumers |

Flow:

```
Producer → Exchange → Queue → Consumer
```

---

## 10. Vikas Mehta: What is persistence in Redis?

**Answer:**
Persistence allows Redis to **save data to disk**, so data isn't lost after a restart.

Redis supports:

* **RDB** (Snapshots)
* **AOF** (Append Only File)

Without persistence, all in-memory data is lost when Redis restarts.
