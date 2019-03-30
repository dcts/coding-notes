# Intro

## JRE / JDK / IDE

- **JRE** (Java Runtime Environment): includes the JVM (java virtual machine) and libraries. To **run** a program!
- **JDK** (Java Development Kit): Includes the java compiler, needed to develop java programs!
- **IDE** (Integrated Development Environment): a program like eclipse or netbeans, that automatically compiles the sourcecode before running the program.

## Compiler

Java is a compiled language, meaning that the source code needs to be transformed into bytecode by the java compiler! After compilation, the program can be run by the java virtual machine! Java files look like this:
- `test.java`: sourcecode written in java-syntax! humanly readible! 
- `test.class`: bytecode (machine code), which can only be read and executed by the java virtual machine!
- `.java` files are usually stored in **src** (source), while `.class` files are stored in **bin** (binary) directory.

## Commandline

```bash
# check if java is installed (shows version)
java -version 

# compiles a .java file (creates .class file)
javac Test.java

# run compiled .class file (no file extension)
java Test
```