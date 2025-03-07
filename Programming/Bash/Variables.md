```bash
#variables are written as the variable name first and then the value of the variable
#only supports lowercase and underscores
#example:
variable=value
language=english
#and then use $variable to call the variable
#example:
cat $variable
ls $language

#to set the variable as a cmdline argument use $1, $2, etc.
#example
variable=$1 #sets the variable as the first argument passed to the command
./test.sh test1
cat $variable #runs cat test1 because test1 was passed as the first command line argument

#to capture input from a command as a variable run the command with "substitution" syntax
#example
variable=$(echo "value")
mkdir $variable
```
[[Bash]]
