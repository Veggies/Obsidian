```bash
#The while loop functions like the python loop. While something, in this case variable, is equal to testing, the loop will set variable to the output of cat /files/test.txt
while [variable="testing"] #must use [] as it's a conditional staatement
do
variable=$(cat /files/test.txt) #must use substitution syntax to run the bash command
done

#Can use
continue #This is useful for when an input not specified is entered. Use the continue option following an else statement and it will restart the while loop
#and
break #breaks out of the loop
```
[[Bash]]