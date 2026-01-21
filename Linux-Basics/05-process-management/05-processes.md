# 🧠 Linux Process Basics

This repository covers **Linux process management fundamentals**, including viewing processes, monitoring system performance, managing foreground/background jobs, and terminating processes. Ideal for **Linux beginners, DevOps engineers, and interview preparation**.

---

## 📌 What is a Process?

A **process** is a running instance of a program. Every process in Linux has a unique **Process ID (PID)** and is managed by the kernel.

---

## 🔹 Viewing Processes

### `ps aux`

Displays a snapshot of **all running processes** in the system.

```bash
ps aux
```

**Options explained:**

* `a` → Show processes for all users
* `u` → User-oriented output
* `x` → Include processes without a terminal

**Important columns:**

* `USER` – Owner of the process
* `PID` – Process ID
* `%CPU` – CPU usage
* `%MEM` – Memory usage
* `COMMAND` – Command that started the process

---

## 🔹 Real-Time Monitoring

### `top`

Shows **live system performance and running processes**.

```bash
top
```

**Key actions inside `top`:**

* `q` → Quit
* `k` → Kill a process by PID

---

### `htop`

An **enhanced version of `top`** with a better UI.

```bash
htop
```

**Features:**

* Colorful and interactive UI
* Mouse support
* Tree view of processes
* Easy process termination

📦 Install `htop`:

```bash
sudo apt install htop
```

---

## 🔹 Killing Processes

### `kill`

Terminates a process using its PID.

```bash
kill PID
```

**Common signals:**

* `kill -15 PID` → Graceful termination (default)
* `kill -9 PID` → Force kill

---

## 🔹 Foreground vs Background Jobs

### ▶ Foreground Job

Runs in the terminal and **blocks user input**.

```bash
sleep 100
```

---

### ▶ Background Job

Runs in the background using `&`.

```bash
sleep 100 &
```

Output example:

```text
[1] 12345
```

* `1` → Job ID
* `12345` → PID

---

## 🔹 Job Control Commands

### `fg`

Bring a background job to the foreground.

```bash
fg %1
```

### `bg`

Resume a stopped job in the background.

```bash
bg %1
```

### Other useful commands

```bash
jobs        # List active jobs
Ctrl + Z    # Suspend a running job
Ctrl + C    # Terminate a job
```

---

## 💡 DevOps / Interview Tip

> Foreground jobs block the terminal, while background jobs allow multitasking using `&`, `fg`, and `bg`.

---

## 📚 Use Cases

* Linux system administration
* DevOps monitoring and troubleshooting
* CI/CD runner process management
* Interview preparation

---

## ⭐ Contribute

Feel free to fork this repository, add examples, or improve documentation.

---

**Happy Learning Linux! 🐧🚀**
