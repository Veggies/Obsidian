```bash
#for loops
#format
for variable in $(cat file) #renames the variable to all lines listed in file until the loop is complete
do
mkdir $variable #makes directory for each line in cat file
done
#specifying range is done using curly braces
{1..100}
```
[[Bash]]