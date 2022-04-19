## Special characteres 

### Do nothing 
: --> is used for doing nothing or can be assumed as true 
#### USe case 1
``` Bash Script 
:
echo $?  ## This will print true /0
```
#### Use case 2 in While 
While true do nothing , Similiar for If 
```
while :
do
operation-1
operation-2
...
operation-n
done

if condition
then : # Do nothing and branch ahead
else # Or else ...
take-some-action
fi
```

#### Use case 4 : Create empty file 
```
: > test.yaml
```

#### Creating Empty Function 
```
: ()
{
echo 'Empty function'
}
```
## Using Variables 
#### Declaring and Printing amd assignment
```
var=1
echo $var
var2 = $var
echo $var2
```
```
hello=375
echo hello # hello
echo $hello # 375

## Duoble quotes will try to get this value 
echo "$hello" # 375
echo "${hello}" # 375

## Single quotes will print this value 

echo '$hello' # $hello
```

```
numbers="one two three"

other_numbers="1 2 3"

```
Check if value of variable is null 
```
if [ -z "$unassigned" ]
then
echo "\$unassigned is NULL."
fi # $unassigned is NULL.
```
### Duoble quotes
preserves (from interpretation) most of the special characters within STRING.


### Single Quotes 
'STRING' preserves all special characters within STRING. This is a stronger form of quoting than "STRING".


### Escape \ sign 
