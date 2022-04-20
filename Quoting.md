### Single Quotes 
This has the effect of protecting special characters in the string from reinterpretation or expansion by the shell or shell script
Single quotes (' ') operate similarly to double quotes, but do not permit referencing variables, since the special meaning of $ is turned off
Within single quotes, every special character except ' gets interpreted literally. Consider single quotes ("full quoting") to be a stricter method of quoting than double quotes ("partial
quoting").

### Duoble Quotes 
When referencing a variable, it is generally advisable to enclose its name in double quotes
This prevents reinterpretation of all special characters within the quoted string -- except $, ` (backquote), and \ (escape).
```
List="one two three"
for a in $List 
do
echo "$a"
done
# Ans --> 
#one
#two
#three  
```
Keeping $ as a special character within double quotes permits referencing a quoted variable
```
List="one two three"
for a in "$List" 
do
echo "$a"
done
# Ans --> # one two three

```
####Running Script with Params 
```
variable1="a variable containing five words"
./test.sh $variable1
This will run script with 7 parameters
```
Using escape sequences with Duoble quotes
```
var2="\\\\\""
echo $var2
# Ans " --> all other things are escaped 
```
```
echo "$var2"
Ans \_\_\"
```
Now using single quotes for same
```
var3='\\\\'
echo "$var3"
# Ans \\\
It always prints whas inside
echo "$(echo '"')"
#Ans --> "


```


