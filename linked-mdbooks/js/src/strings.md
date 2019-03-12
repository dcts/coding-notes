# Strings


```js
// string concatenation
consol.log("Hello " + "World!");

// string interpolation (ES06)
console.log(`my name is "${thomas}"`); // no escaping, better readibility

// escaping
var s  = "this is how you escape doublequotes: \"YAY\"";
var s2 = "this is how you escape backslash: \\";
x = "\'";	// single quote
x = "\""	// double quote
x = "\\"	// backslash
x = "\n"	// newline
x = "\r"	// carriage return
x = "\t"	// tab
x = "\b"	// backspace
x = "\f"	// form feed

// basic string functions
string.length            // retursn length of string (integer)
str.toUpperCase()        // all characters to upper case
str.toLowerCase()        // all characters to lower case

// chosing characters of string
str.charAt(index);    // returns char at index (dot notation)
str[index]            // returns char at index (bracket notation)
str[string.length-1]  // returns last character of string

// substr (second argument = maximum lengt of returned string)
str.substr(index, maxLength) // length of returned string <= maxLength
str.substr(1)                // omitt first character of string

// substring (second argument = index to stop at but not include)
str.substring(index, endPos)
str.substring(1, str.lenght) // omitt first character of string
str.substring(1)             // omitt first character of string

// split -> return array
str = "this is an example!"
str.split(delimitter, maxSplits); // maxSplits <= returned array length

str.split(" ")    // ["this", "is", "an", "example"]
str.split(" ", 2) // ["this", "is"] -> last two cases are thrown away
str.split("");    // separate each character

// split -> get same result as in java "str.split(' ', 2);"
sameResultAsInJava = [str.split(' ')[0], str.split(' ').slice(1).join(' ')]

// check first character
str.startsWith("H");  // returns true or false
```