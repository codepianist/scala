# Scala

## About
- Started in 2003
- Created by Martin Adersky (Java Generics + Java Compiler)
- Runs on JVM, creates Java bytecode
- Java interoperability. Can use any Java library
- Compiles a little bit slow comparing to Java
- It's flexible and opinionless, has several ways to do the same thing and it's entirely up to you to decide:
    - Sometime will be difficult to recognize the Scala exotic syntax
    - You can write imports at the middle of a class
- It leverages freedom: Tell me what to do not How to do.
```
// Java
for(int i=0; i<100; i++){
    System.out.println(i);
}

// Scala
(0 to 100).foreach(println)
```

## Functional and Object Orientated
- Everything is an Object
- There's no primitive types
- There's no static methods or fields
- val defines a fixed variable, like Java constants
- Functions are Objects

### Functional:
- Pure Functions: No side effects.
- Higher Order Functions: Allow pass a function as argument, return functions and store it in a variable.

## Installing:
- [http://www.scala-sbt.org/download.html](www.scala-sbt.org/download.html)
- Via sbt (Linux Debian)
```
echo "deb https://dl.bintray.com/sbt/debian /" | sudo tee -a /etc/apt/sources.list.d/sbt.list
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 2EE0EA64E40A89B84B2DF73499E82A75642AC823
sudo apt-get update
sudo apt-get install sbt
```

## Running:
- Scala Interpreter (REPL/console).
```
sbt console
```
- As shell scripts: 
    - Save the file and run: 
        - `./hello.sh World!` or
        - scala hello.sh World!
```scala
#!/bin/sh
exec scala "$0" "$@"
!#
object Hello {
    def main(args: Array[String]){
        println("Hello Cruel "+ args.toList +"!")
    }
}
Hello.main(args)
```

- Via compiler: scalac.
```
scalac hello.scala
scala hello
```
    



