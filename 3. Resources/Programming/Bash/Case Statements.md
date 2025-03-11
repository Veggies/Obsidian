```bash
#Case statements allow for commands to be ran depending on what the variable equals
case $variable in
1) command
;; #if option = $variable, it will run command
2) cat
;; #etc 
3) ls
;; #etc
*) break
;; etc
esac #must end case with reverse, esac
```
[[Bash]]