## 🐚 Bash Basics – Getting Started

Bash (Bourne Again Shell) is the most commonly used shell in Linux systems.
It allows users to automate tasks, run commands, and write scripts to make system administration easier.

---

## 📌 What is Bash?

Bash is a command-line interpreter that executes commands entered by the user or read from a script file.
It is widely used in Linux, DevOps, CI/CD pipelines, and cloud automation.

# 🔹 Basic Bash Script Example

Below is a simple Bash script that prints a greeting message.
<pre>
📄 Script: script.sh
#!/bin/bash

name="DevOps"
echo "Hello $name"
</pre>

🔹 Explanation
<pre>
Line	Description
#!/bin/bash	Shebang – tells the system to use Bash
name="DevOps"	Assigns a value to a variable
echo "Hello $name"	Prints output to the terminal
</pre>

🔹 Make the Script Executable
Before running a Bash script, you must give it execute permission.
<pre>chmod +x script.sh</pre>

🔹 Run the Script
<pre>./script.sh </pre>

🖥️ Output:
Hello DevOps

## 🔹 Why Learn Bash?
<pre>
✔ Automate repetitive tasks
✔ Essential for Linux & DevOps Engineers
✔ Used in CI/CD pipelines
✔ Improves productivity and system management
</pre>
---
## 📚 Next Topics to Learn

- Variables and Data Types
- User Input (read)
- Conditional Statements (if, else)
- Loops (for, while)
- Functions
- Bash for DevOps Automation

---
## ⭐ Conclusion

Bash scripting is a foundational skill for anyone working with Linux or DevOps.
Start small, practice daily, and gradually build powerful automation scripts.
