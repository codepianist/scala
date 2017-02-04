# Scala

### Variables:
```
// Constant
val team: String= "Corinthians"

// Common variable
var otherTeam: String= "Palmeiras"
var otherTeam= "Corinthians" // Type inference
```



### Operators
```
// Operators are methods
var year= 2000.+(16)

// infix notation
// When a method:
// has 0 or 1 arg, you can drop the '.' and the parenthesis
// has more the 1 arg, you can drop the '.'
year= 2000 + 16
year.toString
2004 toString
```

### Scala number types (no primitives):
- Byte
- Short
- Int
- Long
- Char
- String
- Float
- Double
- Boolean


### Methods:
```
def sum(x: Int, y: Int): Int = {
    return x + y
}

// return is optional
def sum(x: Int, y: Int): Int = {
    x + y
}

// return type can be inferred
def sum(x: Int, y: Int) = {
    x + y
}

// can create it inline too
def sum(x: Int, y: Int) = x + y

// Similar void functions in Java
def prtSum(x:Int, y:Int):Unit = println(x+y)
def prtSum(x:Int, y:Int) { println(x+y) } // same as above 

```

#### Named args:
```
// Both valid
def register(name= "Carlos", surname= "Caramujo")
def register(surname= "Caramujo", name= "Carlos")
```


#### Default values:
```
def register(name: String, surname: String, country: String= "Brasil")
```


#### Passing Fuctions to methods:
```
def test(f: ()=> Boolean):Boolean = {}
```


### Other features:
- Pattern Matching.
- For Comprehensions.
- Currying.
- Functional Literals (tuples).
- Tail Call Optimization(@tailrec).