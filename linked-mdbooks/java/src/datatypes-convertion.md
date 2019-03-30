# Converting Datatypes

```java
// convert -> STRING
String s = Integer.toString(int1);         // int -> String
String s = "" + int1;                      // int -> String
String s = Double.toString(double1);       // double -> String
String s = "" + double1;                   // double -> String
String s = String.format("%.1f", double1); // double -> String (1 decimal place)
String s = new String(chAr);               // char[] -> String
char[] chAr = s.toCharArray();             // String -> char[]

// Array -> String
import java.util.Arrays;  // import Array Class
Arrays.toString(iArr);    // convert

// convert -> INTEGER
Integer.parseInt(s);            // String -> int 
Double.parseDouble(s);          // String -> double
Character.getNumericValue(ch);  // char -> int

// CASTEN
(int)x                // x will be casted to int
(double)x             // x will be casted to double
(datatype)variable    // general syntax
```

