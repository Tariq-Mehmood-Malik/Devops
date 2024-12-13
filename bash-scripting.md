# Bash/ Shell Scripting
It is a way to automate tasks by writing scripts that execute a sequence of commands in a Unix/Linux shell. A shell script is simply a text file that contains a series of commands that are executed by the shell. It's like telling your computer to perform a series of actions automatically.

**`Shell`** Is a program that allows users to interact with the operating system by typing commands.

### Uses of Scripting
- **Automation**: Automate repetitive tasks like backups or file management.
- **Efficiency**: Run complex sequences of commands with a single command.
- **Customization**: Tailor tasks to your needs by combining multiple commands.

### Basic Structure of a Bash Script:
1. **Shebang (`#!/bin/bash`)**: The first line tells the computer that the file should be executed using Bash.
2. **Commands**: These are the same commands you’d run in the terminal.
3. **Variables**: You can store data and use it throughout the script.

---

### Example 1: **Simple "Hello World" Script**

Create a file named `hello.sh`:

```bash
#!/bin/bash
# This is comment

echo "Hello, World!"
```

- **`#!/bin/bash`** tells the computer to use Bash to run the script.
- **`echo "Hello, World!"`** prints the message "Hello, World!" to the terminal.

To run the script:
1. Make the script executable:  
   ```bash
   chmod +x script-name.sh
   ```

2. Run the script:  
   ```bash
   ./script-name.sh
   ```

**Output:**
    ```
    Hello, World!
    ```

---

### Example 2: **Using Variables**

```bash
#!/bin/bash
# This script greets the user

name="John"
echo "Hello, $name!"
```

- **`name="John"`** creates a variable named `name` and stores "John" in it.
- **`echo "Hello, $name!"`** prints "Hello, John!" by using the value stored in the `name` variable.

---

### Example 3: **For Loop**

```bash
#!/bin/bash
# This script prints numbers from 1 to 5

for i in {1..5}
do
  echo "Number: $i"
done
```

- **`for i in {1..5}`** sets up a loop that runs 5 times.
- **`echo "Number: $i"`** prints the value of `i` in each iteration.

**Output:**
```
Number: 1
Number: 2
Number: 3
Number: 4
Number: 5
```

---

### Example 4: **Conditional (If-Else) Statement**

```bash
#!/bin/bash
# This script checks if a file exists

file="/path/to/file.txt"

if [ -f "$file" ]; then
  echo "File exists."
else
  echo "File does not exist."
fi
```

- **`if [ -f "$file" ]`** checks if the file exists.
- **`then`** runs the command if the file exists.
- **`else`** runs the command if the file doesn’t exist.

---

### Example 5: **Accepting User Input**

```bash
#!/bin/bash
# This script asks the user for their name and greets them

echo "What is your name?"
read name
echo "Hello, $name!"
```

- **`read name`** takes input from the user and stores it in the `name` variable.
- **`echo "Hello, $name!"`** greets the user with their name.

---

### Example 6: **Simple Backup Script**

```bash
#!/bin/bash
# This script backs up a directory

src_dir="/home/user/documents"
backup_dir="/home/user/backup"

echo "Starting backup of $src_dir to $backup_dir"
cp -r "$src_dir" "$backup_dir"
echo "Backup completed!"
```

- **`cp -r "$src_dir" "$backup_dir"`** copies all files and subdirectories from `src_dir` to `backup_dir`.

---

### Example 7: **Using Arguments in a Script**

```bash
#!/bin/bash
# This script takes arguments from the command line

echo "First argument: $1"
echo "Second argument: $2"
```

- When you run the script, you pass arguments after the script name.
- **`$1`** and **`$2`** are placeholders for the first and second arguments.

Run the script like this:
```bash
./script.sh arg1 arg2
```

**Output:**
```
First argument: arg1
Second argument: arg2
```
