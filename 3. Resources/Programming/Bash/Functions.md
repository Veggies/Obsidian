```bash
function functionname() {
code here
return 1 #returns an exit code but doesn't exit the script, only the function
}

function add () {
echo $(( $1 + $2 ))
}
sum=$( add $1 + $2 ) #You must use substitution syntax to create a variable from a function inside of a script

functionname #To simply call upon a function
```
[[Bash]]