Bash is a popular Unix shell used for scripting and automating tasks on Unix-based systems like Linux and macOS. 

### Step 1: Setting Up
Before you start, make sure you have a text editor (e.g., nano, vim, or VSCode) and a terminal open.

### Step 2: Create a Bash Script File
In your terminal, use your text editor to create a new file. You can name it something like `myscript.sh`:

```bash
nano myscript.sh
```

### Step 3: Writing Your First Script
Inside the script file, you can start writing Bash commands. For example, let's create a simple script that prints "Hello, World!" to the console:

```bash
#!/bin/bash
# This is a comment
echo "Hello, World!"
```

Here's what's happening:
- `#!/bin/bash`: This is called a "shebang" line, and it tells the system that the script should be interpreted using the Bash shell.
- `# This is a comment`: Comments start with `#` and are ignored by the script. They are useful for documenting your code.
- `echo "Hello, World!"`: This command prints "Hello, World!" to the console.

### Step 4: Make the Script Executable
To run the script, you need to make it executable. In the terminal, run the following command:

```bash
chmod +x myscript.sh
```

This command grants execution permission to the script.

### Step 5: Running the Script
You can now execute your script by typing:

```bash
./myscript.sh
```

You should see "Hello, World!" printed on the terminal.

### Step 6: Variables and User Input
Bash scripts can use variables to store and manipulate data. Let's create a script that takes user input and displays a customized greeting:

```bash
#!/bin/bash
echo "What's your name?"
read name
echo "Hello, $name!"
```

Run the script and see how it prompts for your name and responds accordingly.

### Step 7: Conditional Statements
Bash supports conditional statements like `if`, `else`, and `elif`. Let's create a script that checks if a number is positive or negative:

```bash
#!/bin/bash
echo "Enter a number: "
read number

if [ $number -gt 0 ]; then
  echo "It's a positive number."
elif [ $number -lt 0 ]; then
  echo "It's a negative number."
else
  echo "It's zero."
fi
```

### Step 8: Loops
You can use loops in Bash for repetitive tasks. Here's an example of a `for` loop that prints numbers from 1 to 5:

```bash
#!/bin/bash
for i in 1 2 3 4 5; do
  echo $i
done
```

### Step 9: Functions
Bash allows you to define functions for code reusability:

```bash
#!/bin/bash
# Define a function
say_hello() {
  echo "Hello, $1!"
}

# Call the function
say_hello "Alice"
say_hello "Bob"
```

### Step 10: Command-Line Arguments
You can pass arguments to your script when executing it. These arguments are stored in special variables. Here's an example that takes two numbers as command-line arguments and adds them:

```bash
#!/bin/bash
if [ $# -ne 2 ]; then
  echo "Usage: $0 <number1> <number2>"
  exit 1
fi

sum=$(( $1 + $2 ))
echo "Sum: $sum"
```

Run the script like this:

```bash
./myscript.sh 10 20
```

This will print "Sum: 30" on the terminal.
