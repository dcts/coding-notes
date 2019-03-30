# Strings

```java
String s1 = new String("Hallo Welt");     // Stringvariable
String s2 = "Hallo Welt";                 // Kurzschreibweise
StringBuffer sb  = new StringBuffer();    // Erstellt StringBuffer
StringBuffer sb2 = new StringBuffer(s1);  // Erstellt StringBuffer aus s1
```

## Escaping

```java
System.out.println("\n");      // newline
System.out.println("\t");      // tab
System.out.println("\\");      // backslash
System.out.println("\"");      // double quotes
System.out.println("\'");      // single quotes
System.out.println("\uXXXX");  // inser unicode character

```

## String functions

```java
// teststring
String s = "Hello World";

// basic stringfunctions
s.length();                 // returns 11
s.substring(0,4);           // returns "Hello"


// string comparison
s.equals("HelloWorld!");    // true
s.contains("World");        // true

```

## String Formatting

```java
// print formatted string
System.out.printf();  // no newline!

// store formatted string
float f1 = 2.346f;
String s = String.format("my number: %.2f", f1);

// formatting options
%d    // integer				
%f    // float
%.2f  // float with 2 digits		
%s    // string	
%S    // string in capital letters
%c    // character
%C    // CHARACTER capital print
%b    // boolean
%B    // BOOLEAN capital print

// predefined string length:
%-15s // left align  -> puts spaces at end untill s.length() = 15
%15s  // right align -> puts spaces in front untill s.length() = 15 

// example
String s = String.format("%-15s", "hallo");
```

## String Buffer
```java
// initialize empty string buffer
StringBuffer sb = new StringBuffer();

// initialize string buffer and fill with string str
StringBuffer sb = new StringBuffer(str);

```

 x = alle primitiven Datentypen od. char[]				
 s = String					
 b = StringBuffer					
sb.length();	Länge des StringBuffers b
sb.append(x);	Hängt x an b an
sb.insert(pos, x);	einfügen von x an der Position pos! 
sb.replace(from, to, str);	ersetzt Buffer an Position from bis to mit str.
sb.delete(from, to);		lösche Buffer an der Position from bis to!
sb.setCharAt(pos, 'a');	setzt b[pos] auf 'a'
sb.charAt(pos);	Gibt die Stelle pos von b als char an den Rufer
sb.substring(from);		Liefert Teilstring ab Index from
sb.substring(from, to);	Liefert Teilstring ab Index from bis to 
sb.length();		Länge des Buffers
sb.toString();		Liefert Ihnalt des StringBuffers b als String




s.substring(from);		Liefert Teilstring ab Index from
s.substring(from, to);	Liefert Teilstring ab Index from bis to
s.length();		Liefert Stringlänge
s.contains(s2);		Patternmatching: liefert true/false
int i = s.indexOf(s2);	Patternmatching: Integer i gibt Position wieder (oder -1 falls nicht gefunden)
