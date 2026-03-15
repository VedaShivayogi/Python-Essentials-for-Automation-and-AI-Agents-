# File Handling – Introduction
<details>
<summary>Show more</summary>
    
- **File Handling** is a way of **storing data permanently on secondary storage**
- **File Handling** in Python refers to the processing of **createing, reading, writing, updating, and deleting files** using built-in functions.
- Helps in **data persistence**, even after program execution ends



### Why File Handling is Important?
<details>
<summary>Show more</summary>
    
- Stores data **permanently**
- Avoids **data loss** after program termination
- Handles **large amounts of data efficiently**
- Useful for **real-world applications** like databases, logs, reports 

</details>

### Real-Time Applications
<details>
<summary>Show more</summary>
    
- Saving user registration data
- Reading machine learning datasets
- Log

</details>

### Types of Files
<details>
<summary>Show more</summary>
    
#### 1. Text Files
<details>
<summary>Show more</summary>

**Definition:**
Text files are files that contain human-readable characters encoded using ASCII or Unicode.
Each character is stored as a byte representing letters, numbers, and special symbols.

**Features:**
- Can be opened and read using a normal text editor
- Stored in readable form
- Uses .txt, .log, .md extensions

**Examples:**
.txt, .log, .md
</details>

#### 2. Binary Files
<details>
<summary>Show more</summary>

**Definition:**
Binary files store data in binary format (0s and 1s).
They are not human-readable and require special software or programs to read and interpret them.

**Features:**
- Faster to read/write than text files
- Stores images, audio, video, documents
- Data is machine-readable

**Examples:**
.jpg, .png, .pdf, .mp3, .exe
</details>

#### 3. CSV Files (Comma-Separated Values)
<details>
<summary>Show more</summary>

**Definition:**
CSV files are specialized text files where data is stored in tabular format.
Each row is separated by a newline, and values in a row are separated by commas (or other delimiters).

**Features:**
- Easy to read and write
- Commonly used for data exchange
- Can be opened in Excel and databases

**Examples:**
.csv
</details>

#### Difference Between Text Files, Binary Files, and CSV Files
<details>
<summary>Show more</summary>

| **Parameter**           | **Text Files**                              | **Binary Files**                                    | **CSV Files**                                |
| ----------------------- | ------------------------------------------- | --------------------------------------------------- | -------------------------------------------- |
| **Readability**         | Human-readable (ASCII / Unicode)            | Not human-readable (machine format)                 | Human-readable (structured text)             |
| **Data Representation** | Characters, strings, numbers stored as text | Raw bytes (images, executables, serialized objects) | Tabular data with comma-separated values     |
| **Storage Efficiency**  | Less efficient (larger file size)           | Highly efficient (compact storage)                  | Moderate efficiency (due to delimiters)      |
| **Editing / Viewing**   | Any text editor (Notepad, VS Code)          | Requires specialized tools or programs              | Text editors or spreadsheet software (Excel) |
| **Data Integrity**      | May lose formatting across platforms        | Preserves exact data structure                      | Depends on consistent delimiters and format  |
| **Examples**            | `.txt`, `.log`, `.md`                       | `.jpg`, `.png`, `.pdf`, `.exe`                      | `.csv`                                       |
</details>
</details>

### Types Path of Files
<details>
<summary>Show more</summary>

#### 1. Absolute Path
<details>
<summary>Show more</summary>
    
**Definition:**  
An **absolute path** specifies the complete location of a file starting from the **root directory** of the system.

**Example:** C:\Users\paramesh\Desktop\Delete\file handling.txt


**Characteristics:**
- Starts from the root directory
- Directory independent
- Longer path length
- Harder to type
- More reliable in scripts
</details>

#### 2. Relative Path
<details>
<summary>Show more</summary>

**Definition:**  
A **relative path** specifies the location of a file **relative to the current working directory**.

**Example:**
Delete\file handling.txt

**Characteristics:**
- Depends on the current working directory
- Shorter path length
- Easier to type
- Less reliable in scripts

</details>

#### Difference Between Absolute and Relative Path
<details>
<summary>Show more</summary>
    
| Parameter | Absolute Path | Relative Path |
|--------|---------------|---------------|
| Definition | Complete path from root directory | Path relative to current directory |
| Path Length | Longer | Shorter |
| Directory Dependence | Independent | Dependent |
| Ease of Typing | Harder | Easier |
| Reliability | Reliable in scripts | Unreliable if directory changes |
| Example | `C:\Users\paramesh\Desktop\Delete\file handling.txt` | `Delete\file handling.txt` |


</details>
</details>

### File Operations
<details>
<summary>Show more</summary>

- Create a file  
- Open a file  
- Read data  
- Write data  
- Append data  
- Close the file

#### File Operations using `open()` Function

**Definition**
The `open()` function is used to open a file and returns a **file object**.  
This file object is used to perform read, write, and append operations.

## Syntax
```

file = open("data.txt", "r")
```

### Explanation
- `"data.txt"` → Name of the file  
- `"r"` → Mode (read mode)  
- `file` → File object returned by `open()`

</details> 

### File Modes in Python
<details>
<summary>Show more</summary>
    

  
| Mode | Description |
|------|------------|
| `r` | Read mode |
| `w` | Write mode |
| `a` | Append mode |
| `r+` | Read & Write |
| `b` | Binary mode |
| `t` | Text mode |
</details>


#### Example Program (Create File)
<details> <summary>Show more</summary>

```
    file_name = open("file handling.txt", "x")
```
**Explanation:**

`open("file handling.txt", "x")`
- Opens a file named file handling.txt in exclusive creation mode.
- The "x" mode creates a new file.
- If the file already exists, it raises a FileExistsError.
- file_name
This is a file object that you can use to write to the file using methods like write().
`file_name.close()`
</details>


#### Example Program (Read File)
<details>
<summary>Show more</summary>

```python
file = open("data.txt", "r")
print(file.read())
file.close()
```


#### Explanation:

- `open("data.txt", "r")`  
  Opens the file **data.txt** in **read mode**.  
  The file must already exist.

- `file.read()`  
  Reads the **entire content** of the file as a string.

- `print()`  
  Displays the file content in the output.

- `file.close()`  
  Closes the file and releases system resources.

</details>



#### Example Program (Write File)
<details>
<summary>Show more</summary>

```python
file=open("data.txt","w")
file.write("hello world")
file.close()

```
#### Explanation:

- `open("data.txt", "w")`  
  Opens the file **data.txt** in **write mode** (`"w"`).  
  - If the file **does not exist**, Python creates it.  
  - If the file **already exists**, its content is **overwritten**.

- `file.write("hello world")`  
  Writes the string `"hello world"` into the file.  
  - Note: It **does not automatically add a new line**.

- `file.close()`  
  Closes the file and **saves all changes**, releasing system resources.
</details>


### Python File Reading Methods
<details>
<summary>Show more</summary>
    
#####  1. read()
**Usage:** Reads the entire file as a single string.

**Example:**
```
file = open("file handling.txt", "r")
content = file.read()
print(content)
file.close()
```
**Notes:**
- Reads everything at once.
- Good for small files, not efficient for very large files.

##### 2. readline()
**Usage:** Reads one line at a time from the file.

**Example:**
```
file = open("file handling.txt", "r")
line1 = file.readline()
line2 = file.readline()
print(line1)
print(line2)
file.close()
```
**Notes:**
- Each call reads the next line.
- Useful for line-by-line processing.

##### 3. readlines()
**Usage:** Reads all lines and returns a list of strings, where each string is a line.

**Example:**
```
file = open("file handling.txt", "r")
lines = file.readlines()
print(lines)
file.close()
```
**Notes:**
- Returns a list, e.g., ["Line1\n", "Line2\n"].
- Easier for iterating through lines using loops:

**Method	Returns	Reads**
read()	Single string	Entire file
readline()	Single line string	One line at a time
readlines()	List of strings	All lines
</details>

#### Program: Read or Reading File and Splitting Words
<details><summary>Show more</summary>
    
```
file_name = open("file handling.txt", "r")
anything = file_name.read()
for i in anything.split():
    print(i)
file_name.close()
```


**Explanation**
`open("file handling.txt", "r")`
Opens the file in read mode.

`file_name.read()`
Reads the entire content of the file and stores it in the variable anything.

`anything.split()`
Splits the text into individual words using spaces as separators.

`for i in anything.split():`
Loops through each word in the file.

`print(i)`
Prints one word per line.

`file_name.close()`
Closes the file to free memory and resources.
</details>

#### Program: Reading File Using readlines()
<details><summary>show more</summary>

```
file_name=open("file handling.txt","r")
for i in file_name.readlines():
    print(i,end="")
    file_name.close()
```
**Explanation**

`open("file handling.txt", "r")`

Opens the file in read mode.

`file_name.readlines()`

Reads all lines from the file and returns them as a list.

`for i in file_name.readlines():`

Goes through the file line by line.

`print(i, end="")`
Prints each line.
end="" prevents extra blank lines.

`file_name.close()`
Closes the file after reading is completed.
</details>


#### Display lines in a file which word "GPT" in it
<details><summary>Show more</summary>

```
f1=open("file handling.txt","r")
count=0
lines=f1.readlines()
for i in lines:
    if(i.count("GPT")>0):
        print(i)
f1.close()
```

**Explanation**

`f1 = open("file handling.txt", "r")`
- Opens the file in read mode.
- Allows reading text from the file

`lines = f1.readlines()`
- Reads all lines from the file.
- Stores them as a list of strings.

`for i in lines:`
- Loops through the file line by line.

`if i.count("GPT") > 0:`
- count("GPT") returns the number of times "GPT" appears.
- If greater than zero, the word exists in that line.

`print(i)`
- Prints only lines that contain "GPT".

  </details>
</details>
