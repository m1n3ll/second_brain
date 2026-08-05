## Docker

Difficulty: Beginner

Estimated Reading Time: 5 minutes

### Goal

Understand what Docker is, why it was created, and why it has become one of the most important tools in modern software development.


### Why?

Imagine you develop an application on your laptop.
Everything works perfectly.
You send the project to a friend.
They try to run it...

```
Error:
Module not found.
```

Or maybe:

```
Python version not supported.
```

Or:

```
Connection refused.
```

The application itself isn't necessarily broken. The environment is different.

This problem became so common that developers jokingly started saying:

> "It works on my machine."

Docker was created to solve this problem.

### What?

Docker is an open-source containerization platform that packages an application together with everything it needs to run, including:

- Source code
- Libraries
- Dependencies
- Runtime
- Configuration

This package is called a **container**.

Because the container carries everything it needs, the application behaves consistently across different environments.

### How?

Docker creates isolated environments called **containers**.
Instead of installing software directly on the operating system, the application runs inside its own container.
Each container contains everything the application needs while sharing the host operating system's kernel.
This makes containers lightweight, portable, and fast to start.

### Mental Model

Think of Docker as a shipping company.

Without Docker:
You send the furniture.
Hopefully the destination already has the correct house.

With Docker:
You send the entire furnished apartment.
Wherever it arrives, everything is already inside.
The container always contains the same environment.

### Connections

Application
        ↓
Docker
        ↓
Container
        ↓
Image
        ↓
Docker Engine

### Practical Example

Suppose you build a Flask web application.
Without Docker:

Every developer must install:

- Python
- Flask
- Dependencies
- Environment variables

With Docker:

The application and all of its dependencies are packaged into a single container.

Anyone with Docker installed can run the application using a single command.

```bash
docker run my-flask-app
```

---

### Common Misconceptions

Docker is **not** a virtual machine.

Docker is **not** an operating system.

Docker does **not** replace programming languages or frameworks.

Docker is a platform that packages and runs applications inside containers.


### Key Takeaways

- Docker packages applications with everything they need.
- Docker improves portability.
- Containers are isolated environments.
- Applications behave consistently across different machines.