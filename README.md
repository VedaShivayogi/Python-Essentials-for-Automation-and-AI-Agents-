# Python Essentials for Automation and AI Agents Notes

# 📂 File Handling in Python

## 📌 Introduction

**File Handling** is a method of storing data permanently on secondary storage.

In Python, file handling allows you to:

* Create files
* Read files
* Write files
* Update files
* Delete files

It ensures **data persistence**, even after program execution ends.


## ❓ Why File Handling is Important

* ✅ Stores data **permanently**
* ✅ Prevents **data loss**
* ✅ Handles **large data efficiently**
* ✅ Used in **real-world applications**

  * Databases
  * Logs
  * Reports



## 🌍 Real-Time Applications

* Saving user registration data
* Reading machine learning datasets
* Log file analysis


## 📁 Types of Files

### 1. 📄 Text Files

**Definition:**
Human-readable files stored using ASCII/Unicode.

**Features:**

* Readable in text editors
* Stores plain text

**Examples:**
`.txt`, `.log`, `.md`



### 2. 🧠 Binary Files

**Definition:**
Stores data in binary format (0s and 1s).

**Features:**

* Not human-readable
* Faster processing
* Used for multimedia & executables

**Examples:**
`.jpg`, `.png`, `.pdf`, `.mp3`, `.exe`



### 3. 📊 CSV Files

**Definition:**
Stores tabular data separated by commas.

**Features:**

* Easy to read/write
* Used in Excel and databases

**Examples:**
`.csv`



## 🔍 Difference Between File Types

| Feature     | Text Files     | Binary Files     | CSV Files         |
| ----------- | -------------- | ---------------- | ----------------- |
| Readability | Human-readable | Not readable     | Human-readable    |
| Data Format | Text           | Raw bytes        | Tabular           |
| Efficiency  | Low            | High             | Medium            |
| Tools       | Text editors   | Special software | Excel/Text editor |



## 📍 File Paths

### 1. Absolute Path

**Definition:** Full path from root directory

**Example:**

```
C:\Users\veda\Desktop\Delete\file handling.txt

```

**Features:**

* Independent of directory
* More reliable


### 2. Relative Path

**Definition:** Path relative to current directory

**Example:**

```
Delete\file handling.txt
```

**Features:**

* Shorter
* Depends on working directory


## ⚙️ File Operations

* Create file
* Open file
* Read data
* Write data
* Append data
* Close file


## 🧩 open() Function

**Definition:**
Used to open a file and returns a file object.

### Syntax

```python
file = open("data.txt", "r")
```


## 📌 File Modes

| Mode | Description  |
| ---- | ------------ |
| r    | Read         |
| w    | Write        |
| a    | Append       |
| r+   | Read & Write |
| b    | Binary       |
| t    | Text         |


## 🧪 Example Programs

### ✅ Create File

```python
file_name = open("file handling.txt", "x")
file_name.close()
```


### ✅ Read File

```python
file = open("data.txt", "r")
print(file.read())
file.close()
```


### ✅ Write File

```python
file = open("data.txt", "w")
file.write("hello world")
file.close()
```

## 📖 File Reading Methods

### 1. read()

Reads entire file

```python
file.read()
```

### 2. readline()

Reads one line

```python
file.readline()
```

### 3. readlines()

Reads all lines as list

```python
file.readlines()
```


## 🔍 Example: Split Words from File

```python
file_name = open("file handling.txt", "r")
data = file_name.read()

for word in data.split():
    print(word)

file_name.close()
```


## 📜 Example: Read Lines Using readlines()

```python
file_name = open("file handling.txt", "r")

for line in file_name.readlines():
    print(line, end="")

file_name.close()
```


## 🔎 Example: Find Lines Containing "GPT"

```python
f1 = open("file handling.txt", "r")

for line in f1.readlines():
    if "GPT" in line:
        print(line)

f1.close()
```


