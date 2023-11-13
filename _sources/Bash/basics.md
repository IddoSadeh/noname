# Bash Scripting Basics

The language we have been using to communicate with our command line is called `Bash`. It is a command line interpreter for linux. A command line interprater is often referred to as *shell*. A shell is both a *command language* and a *scripting language*.

We've mainly used Bash as a command language, using Bash as a scripting language will open many doors in our journey.

## Basic Syntax


### **Basic Commands:**

We've used a lot of one liners up until know, some of them are:
   - **`echo`**: Prints text to the terminal.
     ```bash
     echo "Hello, World!"
     ```
   - **`pwd`**: Prints the working directory.
   - **`ls`**: Lists files and directories.
   - **`cd`**: Changes the directory.
   - **`mkdir`**: Creates a new directory.
   - **`touch`**: Creates a new file.
   - **`rm`**: Deletes files and directories.
   


## Scripting

When we want to use bash for scripting, we will do it in a separate file. 

### Quick Example
   - Create a new file with a `.sh` extension (e.g., `script.sh`) and add the following:
     ```bash
     #!/bin/bash
     echo "Hello, World!"
     ```
   - Make the script executable:
     ```bash
     chmod +x script.sh
     ```
   - Run the script:
     ```bash
     ./script.sh
     ```

### More Bash 

Since we are writing larger pieces of code we may find some of the following things useful:

#### Variables
   - Defining variables:
     ```bash
     name="John"
     ```
   - Accessing variables:
     ```bash
     echo $name
     ```

#### Control Flow

   - **Conditional Statements:**
     ```bash
     if [ "$name" == "John" ]; then
       echo "Hi John!"
     fi
     ```
   - **Loops:**
     ```bash
     for i in {1..5}
     do
       echo $i
     done
     ```

#### Input and Output

   - Reading input with `read`:
     ```bash
     #!/bin/bash
     echo "What's your name?"
     read name
     echo "hey ${name}"
     ```
   - Write to a file:
     ```bash
     #!/bin/bash
     echo "What's your name?"
     read name
     echo "hey ${name}" > usersname.txt
     ```  
   - Appending to a file:
     ```bash
     #!/bin/bash
     echo "What's your name?"
     read name
     echo "hey ${name}" >> usersname.txt
     ``` 
   - Similary if we are only writing bash in the command line we can save the output we would normally see in to a file:

    ping -c 4 8.8.8.8 > output.txt



#### Functions

   - Defining and calling functions:
     ```bash
     function greet {
       echo "Hello, $1!"
     }
     
     greet "Alice"
     ```

### More

The options of using Bash are infinite, a good starting point is [freeCodeCamp](https://www.freecodecamp.org/news/bash-scripting-tutorial-linux-shell-script-and-command-line-for-beginners). At the bottom of this page you can learn about automating scripts and debugging code.

<!-- I downloaded this too -->


## Some Fun

An API is an application program interface, generally an API allows us to communicate with software.

Many websites like Reddit and Twitter will have an API that will explain how to use code to interact with the platforms. To get to know how to use API's we can start off with [Public REST API's](https://documenter.getpostman.com/view/8854915/Szf7znEe#86a5b520-e907-4eee-95fd-6dcdc24f8a83) which are free.

Try out this code as an example:

```bash
#!/bin/bash

# Function to fetch and display a random joke
get_joke() {
    JOKE_JSON=$(curl -s "https://official-joke-api.appspot.com/random_joke")
    SETUP=$(echo $JOKE_JSON | jq -r '.setup')
    PUNCHLINE=$(echo $JOKE_JSON | jq -r '.punchline')
    echo -e "$SETUP\n$PUNCHLINE"
}

# Get and display a random joke
get_joke
```

Can you print several jokes at once using a loop? Can you print the jokes to a file? Can you ask the user how many jokes they want? What about using other API's?