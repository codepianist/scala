# Scala

#### Singleton Classes:
- Use object to define a Singleton Class.
```
object Highlander {
    def sayIt(){
        println "With heart, faith and steel. In the end there can be only one!"
    }
    def main(args: Array[String]){
        Highlander.sayIt()
    }
}
```
- Members of a Singleton objects are in fact static although Scala don't have a static keyword. Any member of the singleton object will be reused by all code the uses this object, it will be globally available.


#### Companion Objects:
- When you write a class and an object within the same file, the object is known as a Companion Object.
```
class Sale(){

}
object Sale(){

}
``` 

- You can use Companion Objects to share a static behavior or property:
```
class Product(val name: String, val price: Double) {
    private val id= Product.nextID()
}
// This Companion Object is a Singleton
object Product{
    private var ID= 0
    private def nextID() = {
        ID+= 1
        ID
    }
}
```
- Other usages of Companion Objects are:
    - Functions: they don't depend on any class field, so they may belong to the Singleton Object, so you can separate Functions and Methods.
    - Factory methods. When using factory methods you can turn the primary constructor private like above.
```
// class Product(val name: String, val price: Double) {
class Product private(val name: String, val price: Double) {
    private val id= Product.nextID()
}
// This Companion Object is a Singleton
object Product{
    // Scala use apply methods when you don't use new keyword
    def apply(name: String, price: Double) = new Product(name, price)
    
    def main(args: Array[String]){
        // Both above are valid
        Product.apply("Chocolate Bar 200g", 8.80)
        Product("Chocolate Bar 200g", 8.80) // Scala will look for the apply method within your companion object
    }
    
    private var ID= 0
    private def nextID() = {
        ID+= 1
        ID
    }
}
```