# Scala

### Class hierarchy:
- abstract scala.Any: At the top  
    - Methods:
```
final def ==(that: Any): Boolean // equivalent to Java equals
// Compares objects (equals method)
new String("a") == new String("a") // true in Scala
new String("a").equals( new String("a") ) // true in Java

// eq is equivalent to == in Java
// Compares references
new String("a") eq new String("a") // false in Scala
new String("a") == new String("a") // false in Java

final def !=(that: Any): Boolean
def equals(that: Any): Boolean
def ##: Int
def hashCode: Int
def toString: String
```

- abstract scala.AnyVal extends Any: supertype of all value types
    - Int, Double, Boolean, ..., Unit
    - Can be defined as literals: 51, 11L, .75, ... (Allocated in the heap in Scala)
    - Unit represents an uninteresting result (like a void method in Java)
        - Has 1 value: `var unit:Unit= ()`
        
- abstract scala.AnyRef extends Any: supertype of all reference types
    - Pointer types, can be referenced and dereferenced
    - Equivalent to java.lang.Object
    
- abstract scala.Null extends AnyRef: 

- abstract scala.Nothing extends Any: 


### ScalaDoc:
- It follows the same pattern as JavaDoc.
- Documentation: [http://www.scala-lang.org/api/](www.scala-lang.org/api/)