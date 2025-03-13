```bash
echo ${var} #This sort of seems like how f strings work in python
echo "Here's a test $vartest" #This won't work because vartest isn't a variable, and you would need a space delimiter to seperate var and test
echo "Here's a test ${var}test" #The curly braces "protects" the variable


#Tabs, spaces, or linebreaks in a string will be considered different elements
string="One Two Three" 
for element in ${string}; do #Because the expanded variable isn't in double quotes, the variable is "split" into different elements
echo ${element}
done

#Will print
One
Two
Three

for element in "${string}"; do #Because the expanded variable is in double quotes, the variable is not split into different elements
echo ${element}
done

#Will print
One Two Three
```