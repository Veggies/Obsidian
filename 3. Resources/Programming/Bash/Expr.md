```bash
#use the expr command to perform airthmetic operations. +, -, /, and \* for multipication, you must use a backslash to escape the * from being used a wildcard
expr 5 + 6
expr 5 - 6
expr 5 / 6
expr 5 \* 6
# using double paratheses allows the use of * without a blackslash and pre increment/deicrement and doesn't require expr to be used
#^^^ research pre increment/deincrement
((5 + 6 )) #I think spaces have to follow the (()) for the operation to function
(( 5 * 6 ))

#floating point opertions with bc -l
#-l loads math library, bc is a basic calculator, you have to put it into an echo command in order for it to work because you're piping the outpit into the bc.
#example:
echo "5 / 4" | bc -l
1.25000000000000
```
[[Bash]]
