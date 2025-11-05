## Sheban part

- `#!/bin/bash`

script executor we have to decalre and make sure it is correct otherwise the script trwos deffrent errors.
we have to choose dash or bash or sh among them mostly.
---
## Metadata information part

that contains the autor, date, version, script description like what it does in the comments.

###########################

# #Author: prasanth kumar kankati

# #Date: 05-11-2025

# #version: V1

###########################
---
## Set Debug mode / use echo to segeregate the outputs of commands while it is printing to console:

- `set -x`
free
prints memory 
df -h
prints disk file
ncpus
---
- `set-e`
if any comand is failed the script, execution will gets break to execute further. So on a right time when the error occurs it stops execution.

create a folder , add user, add permission is there in case if the mkdirr command failed whats the point in executing further so it stops at right time.

---
- `set-o pipefail`
we should use set -e & set -o pipefail together to avoid pipe fail errors depends on previous command false error input to next command.

for example 

asasasas | echo 

first command failed but without set-o echo still exectes feeling that the first command still giving the input to the next so execution goes 
so keeping them together will still breaks the execution even there are pipes on a error.

some people simply right and we can alao write 

`set -exo pipefail`

but for modifications and easiness we can define them individially is the best practice.

----

if not used debug mode all the outputs gets mixed up.


---
## Grepping

pf -ef | grep "amazon"

grepping from the list of processes amzon related processes are filtered out. piping takes the input from first command output and takes as input.
---

##AWKing

pf -ef | grep "amazon" | awk -F ','{print$2}'

prints pid present in the second column

Alright, let’s keep it clean and clear 👇

`awk` is a **powerful text-processing tool** in shell scripting. It’s mainly used to **search, filter, and format text or data** — especially useful when dealing with structured text like logs, CSVs, or command outputs.

### 💡 Basic Idea

Think of `awk` as a **mini programming language** built for handling text files line by line and splitting them into **fields (columns)**.

---

### ⚙️ How it Works

* It reads input **line by line**.
* Each line is **split into fields** using a **delimiter** (default: space).
* You can perform **actions** on those fields using patterns or conditions.

---

### 🧱 Basic Syntax

```bash
awk 'pattern { action }' filename
```

or

```bash
command | awk 'pattern { action }'
```

---

### 🔍 Examples

**1️⃣ Print the first column of a file**

```bash
awk '{print $1}' file.txt
```

👉 `$1` = first field (column)
👉 `$0` = whole line

---

**2️⃣ Print specific columns (like name and age)**

```bash
awk '{print $1, $3}' data.txt
```

Prints first and third columns separated by space.

---

**3️⃣ Print lines matching a condition**

```bash
awk '$3 > 50 {print $1, $3}' marks.txt
```

Prints name and marks of students scoring more than 50.

---

**4️⃣ Use a custom delimiter (like comma for CSV)**

```bash
awk -F',' '{print $2}' file.csv
```

`-F','` sets the field separator to comma.

---

**5️⃣ Count lines**

```bash
awk 'END {print NR}' file.txt
```

👉 `NR` = Number of Records (lines processed)

---

### 🚀 Why Use `awk`

* Quick text extraction and transformation
* No need for complex scripts
* Combines well with other commands like `grep`, `sort`, and `sed`

---

## curling

Curl command retrives the content in the URL

curl www.azure.blob/app.log | grep "error"
cat text.log | grep "error"














