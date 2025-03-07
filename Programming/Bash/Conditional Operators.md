```bash
#conditional operators
#must be contained in [] brackets, [[]] is extended attributes
#example
[[ "apple" = "apple" ]] #You HAVE TO PUT SPACES before the END of the square brackets, just like the example!!!
[[ 1 -eq 1 ]]
= #checks if string equals string
!= #if string does not equal strings
-eq #if int equals int
-ne #if int not equal int
-gt #greater than
-lt #less than
&& #checks if both conditions are true when using []
|| #checks both conditions are true when using [[]]

#file level conditional operators
-e #exits
-d #is directory
-s #is not empty
-x #is executable
-w #is writable
#example:
[ -e filename ] #check if the file "filename" exists
```
[[Bash]]