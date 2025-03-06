```bash
if "statement"
then
elif
else
```

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

#to prompt for an input after running a command use the read function
read variable #this provides the user for the command by presenting a blank input in the shell
read -p "Input a variable" variable #presents "Input a variable" when awaiting input. The -p argument provides this functionality

#use the expr command to perform airthmetic operations. +, -, /, and \* for multipication, you must use a backslash to escape the * from being used a wildcard
expr 5 + 6
expr 5 - 6
expr 5 / 6
expr 5 \* 6
# using double paratheses allows the use of * without a blackslash and pre increment/deicrement and doesn't require expr to be used
#^^^ research pre increment/deincrement
(( 5 + 6 )) #I think spaces have to follow the (()) for the operation to function
(( 5 * 6 ))
```
