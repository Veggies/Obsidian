```Bash
#to capture input from a command as a variable run the command with "substitution" syntax
#example
variable=$(echo "value")
mkdir $variable

#to prompt for an input after running a command use the read function
read variable #this provides the user for the command by presenting a blank input in the shell
read -p "Input a variable" variable #presents "Input a variable" when awaiting input. The -p argument provides this functionality
```
[[Bash]]