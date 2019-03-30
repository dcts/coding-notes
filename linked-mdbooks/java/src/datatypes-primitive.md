# Primitive Datatypes

```java
byte byte1 = 127;                   // Byte [-128, 127]
short short1 = 32000;               // Short [-32'000, 32'000]
int int1 = 2100000000;              // Integer [-2.1 Mia, 2.1 Mia]
long long1 = 9200000000000000000L;  // Long [-9.2 Trio, 9.2 Trio], with "L"
float float1 = 3.14f;               // Float, add "f" at end
double double1 = 3.14157;           // Double (higher precision)
boolean boolean1 = (10>2);          // bollean [true, false]
char char1 = 'a';                   // Character
char char2 = '\uXXXX';              // Character (UNICODE STYLE)
String s1 = "hello!";               // String (NOT A PRIMITIVE TYPE)
```

```java
// DECLARATION
double taxRate;
```

```java
// INITIALIZATION
taxRate = 0.57;
```

```java
// IMMUTABLE VARIABLES -> CONSTANTS
final float pi = 3.14f;
```

```java
// GLOBAL VARIABLES
static int count = 0;          // visible inside the class
static final float pi = 3.14f; // global constant
```


