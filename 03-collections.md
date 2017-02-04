# Scala

### Collections:
```
// Imutable Collections
var list= List("c","o","d","e")
var map= Mapq(1-> "c",2-> "o",3-> "d",4-> "e")
list.foreach(v => println(v))
list.foreach(println) // Like method references in Java
for(v <- list) println
```

- Support for generics Covariation/Controvariation:
    - 
    
- Support varargs
```
def add(names: String*) 
```
