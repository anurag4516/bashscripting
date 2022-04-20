#### Exit Command
The exit command terminates a script
Every command returns an exit status (sometimes referred to as a return status or exit code).
A successful command returns a 0, 
while an unsuccessful one returns a non-zero value that usually can be interpreted as an error code
$? reads the exit status of the last command executed
```
echo hello
echo $? # Exit status 0 returned because command executed successfully.
lskdf # Unrecognized command.
echo $? # Non-zero exit status returned -- command failed to execute.
```
Exit status of true & false
```
true # The "true" builtin.
echo "exit status of \"true\" = $?"   Ans # 0
! true
echo "exit status of \"! true\" = $?" Ans  # 1
# Note that the "!" needs a space between it
```
