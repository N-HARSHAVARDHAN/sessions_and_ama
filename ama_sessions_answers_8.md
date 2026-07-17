# 1. RabbitMQ is written in which language?

RabbitMQ is primarily written in **Erlang**, a programming language designed for highly concurrent, fault-tolerant, and distributed systems.

**Why Erlang?**

* High concurrency
* Fault tolerance
* Distributed communication
* Hot code upgrades (without stopping the server)

---

# 2. Difference between Docker and Kubernetes

| Docker                           | Kubernetes                               |
| -------------------------------- | ---------------------------------------- |
| Containerization platform        | Container orchestration platform         |
| Creates and runs containers      | Manages containers                       |
| Runs containers on a single host | Manages containers across multiple hosts |
| No auto scaling                  | Supports auto scaling                    |
| No self-healing                  | Automatically restarts failed containers |
| Manual deployment                | Automated deployment and updates         |

**In short:**

* **Docker** is used to build, package, and run containers.
* **Kubernetes** is used to deploy, scale, and manage those containers in production.

---

# 3. What is a Promise in JavaScript?

A **Promise** is an object that represents the eventual completion (success) or failure of an asynchronous operation.

**Promise States**

* Pending
* Fulfilled
* Rejected

Example:

```javascript
fetch("https://jsonplaceholder.typicode.com/users/1")
.then(response => response.json())
.then(data => console.log(data))
.catch(error => console.log(error));
```

**Benefits**

* Cleaner asynchronous code
* Avoids callback hell
* Better error handling

---

# 4. Why does Apache Kafka have 2 ports?

Kafka often exposes multiple ports because different listeners or services handle different types of communication.

Common examples:

* **9092** → Client communication with Kafka Broker
* **9093/9094** → SSL/SASL or another configured listener

In older Kafka deployments:

* **9092** → Kafka Broker
* **2181** → ZooKeeper communication

**Purpose**

* Separate internal and external communication
* Support secure and non-secure connections
* Allow multiple listeners for different clients

---

# 5. Why do we use a Dockerfile?

A **Dockerfile** is a text file containing instructions for building a Docker image.

It automates:

* Installing dependencies
* Copying application files
* Setting environment variables
* Running commands
* Starting the application

Example:

```dockerfile
FROM python:3.12

WORKDIR /app

COPY . .

RUN pip install -r requirements.txt

CMD ["python","app.py"]
```

**Benefits**

* Reproducible builds
* Easy deployment
* Version-controlled environment
* Eliminates "works on my machine" issues

---

# 6. What is an Execution Context in JavaScript?

An **Execution Context** is the environment in which JavaScript code is executed.

It contains:

* Variables
* Functions
* Scope information
* Value of `this`

**Types**

* Global Execution Context
* Function Execution Context
* Eval Execution Context (rare)

Example:

```javascript
let x = 10;

function greet(){
    console.log(x);
}

greet();
```

JavaScript creates a Global Execution Context first, then a Function Execution Context when `greet()` is called.

---

# 7. What is Celery Beat?

Celery Beat is the **scheduler** of Celery. It periodically sends scheduled tasks to Celery workers based on a defined schedule.

**Use cases**

* Send daily emails
* Database cleanup
* Generate reports
* Refresh cache
* Run cron-like jobs

Example:

```python
CELERY_BEAT_SCHEDULE = {
    "daily-report": {
        "task": "reports.tasks.generate_report",
        "schedule": crontab(hour=9, minute=0),
    },
}
```

---

# 8. Command to see all Docker containers

Show running containers:

```bash
docker ps
```

Show all containers (running and stopped):

```bash
docker ps -a
```

Useful commands:

```bash
docker ps -q
```

Shows only container IDs.

---

# 9. What is `.flat()` in JavaScript?

The `.flat()` method creates a new array by flattening nested arrays up to a specified depth.

Example:

```javascript
const arr = [1, [2, 3], [4, [5]]];

console.log(arr.flat());
// [1,2,3,4,[5]]

console.log(arr.flat(2));
// [1,2,3,4,5]
```

**Benefits**

* Removes nested arrays
* Simplifies array manipulation
* Returns a new array without modifying the original

---

# 10. Why can't we use Docker alone in production?

Actually, **Docker can be used in production**. However, Docker alone does not provide features needed for managing large-scale applications.

Docker lacks:

* Auto scaling
* Self-healing
* Load balancing
* Rolling updates
* Service discovery
* Cluster management

That's why tools like **Kubernetes** are commonly used alongside Docker.

---

# 11. What is slicing in Python?

Slicing is the process of extracting a portion of a sequence such as a string, list, or tuple.

**Syntax**

```python
sequence[start:end:step]
```

Example:

```python
name = "Harsha"

print(name[1:5])
```

Output:

```
arsh
```

Example with list:

```python
nums = [10,20,30,40,50]

print(nums[1:4])
```

Output:

```
[20,30,40]
```

---

# 12. What is RabbitMQ?

RabbitMQ is an **open-source message broker** that enables asynchronous communication between applications by sending messages through queues.

It follows the **Producer → Exchange → Queue → Consumer** model.

Flow:

```
Producer
    ↓
 Exchange
    ↓
   Queue
    ↓
 Consumer
```

**Use cases**

* Email notifications
* Background task processing
* Order processing
* Logging systems
* Communication between microservices

**Benefits**

* Asynchronous processing
* Reliable message delivery
* Decouples services
* Improves scalability
