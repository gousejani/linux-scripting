# 🐚 Shell Scripting Basics

Shell scripting allows you to automate tasks using the Unix/Linux shell.

---

## 📄 Basic Structure of a Shell Script

```bash
#!/bin/bash

# This is a comment
echo "Hello, World!"
```

- `#!/bin/bash`: Shebang line tells the OS to use Bash shell.
- `#`: Starts a comment.
- `echo`: Prints to terminal.

---

## 🏁 How to Run a Shell Script

1. Create the script file:

```bash
nano myscript.sh
```

2. Make it executable:

```bash
chmod +x myscript.sh
```

3. Run it:

```bash
./myscript.sh
```

---

## 🔤 Variables

```bash
name="GJ"
echo "Hello, $name"
```

- No spaces around `=`.
- Access variables using `$`.

---

## 🧮 Arithmetic

```bash
a=5
b=3
sum=$((a + b))
echo "Sum is $sum"
```

---

## 📜 Conditionals

```bash
if [ $a -gt $b ]; then
  echo "a is greater"
else
  echo "b is greater"
fi
```

### Operators:
| Operator | Meaning        |
|----------|----------------|
| `-eq`    | equal          |
| `-ne`    | not equal      |
| `-gt`    | greater than   |
| `-lt`    | less than      |
| `-ge`    | greater or equal |
| `-le`    | less or equal  |

---

## 🔁 Loops

### For Loop

```bash
for i in 1 2 3 4 5
do
  echo "Number $i"
done
```

### While Loop

```bash
count=1
while [ $count -le 5 ]
do
  echo "Count is $count"
  count=$((count + 1))
done
```

---

## 📥 Reading Input

```bash
echo "Enter your name:"
read username
echo "Hi, $username!"
```

---

## 📂 File Checks

```bash
if [ -f "file.txt" ]; then
  echo "File exists"
fi
```

### File Test Operators:

| Test    | Description       |
|---------|-------------------|
| `-f`    | Regular file       |
| `-d`    | Directory          |
| `-e`    | Exists             |
| `-r`    | Readable           |
| `-w`    | Writable           |
| `-x`    | Executable         |

---

## 🧰 Useful Commands

| Command | Description             |
|---------|-------------------------|
| `echo`  | Print text              |
| `read`  | Read user input         |
| `cd`    | Change directory        |
| `ls`    | List files              |
| `pwd`   | Print working directory |
| `mkdir` | Make a directory        |
| `rm`    | Remove file             |

---

## 📌 Sample Script

```bash
#!/bin/bash

echo "Enter a filename:"
read file

if [ -e "$file" ]; then
  echo "File $file exists."
else
  echo "File $file does not exist."
fi
```

---
