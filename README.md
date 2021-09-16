# dotproperties
my first working lexer... .properties class for C++ 
# how to use
```cc
#include <iostream>
#include "dotproperties.hh"
int main() {
  Properties props; // dotproperties class
  props.readFromFile("myprops.properties"); // read props from file
}
``` 
the code above will read from a file, or if you want to read from a string in memory: 
```c
props.read(str);
``` 
and to read properties: 
```cc
props["propname"]
```
want to know if a property exists? 
```cc
props.propertyExists("propname")
```
or how to set a property's content? 
```cc
props.setProperty("propname", "value") // this even creates the property if it doesnt exist
```
finally, if you want to convert your properties into a string
```cc
props.stringify()
```
