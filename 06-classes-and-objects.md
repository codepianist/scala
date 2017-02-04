# Scala:

### Classes:
- if val is used, fields are declared final and no setter is created
- if var is used, getter and setters are created
- if neither val or var is used, no getter or setter are created and the variable will be only visible within the constructor

#### Primary Constructor:
```
// val-> tells the compiler to treat the variable as final fields
// Creates the get method
class Product(val name:String, val price: Double){

}
object Product{
    def main(args: Array[String]){
        val antiVirus= new Product("AntiVirus- Basic", 39.90)
    }
}
```

- Even when you don't define the a implicity primary constructor is created.
```
class Validator{

}
```


#### Additional Constructors:
- use this to create an addittional constructor
- use this to reference even the primary constructor
```
class Client(name: String, email: String, phone: String) {
    def this(name: String, email: String){
        this(name, email, "")
    }
}
object Client {
    def main(args: Array[String]){
        new Client("Sarah", "sarah@test.com")
    }
}
```


#### Getter and Setters:
```
// Creates the get/set
// set is created as id_
class Product(val name:String, val price: Double){
    var id= 0 // creates a public getter and setter
    // public def id():Int
    // public def id_=(y:Int) -> Note id_= is the name of the method
    private var age= 0 // creates a private getter and setter
}
object Product{
    def main(args: Array[String]){
        val antiVirus= new Product("AntiVirus- Basic", 39.90)
        antiVirus.id_= 99989 // use created setter
        antiVirus.id= 99989 // use a shorthand
    }
}
```

- Private can be used on contructor:
```
class Product(private var name: String, private var price: Double){}
```

##### Overriding:
```
class Product(val name:String, val price: Double){
    private var _id= 0
    def id= _id
    def id_(value: Int){
        _id = value*2
    }
}
object Product{
    def main(args: Array[String]){
        val antiVirus= new Product("AntiVirus- Basic", 39.90)
        antiVirus.id= 99989
    }
}
```



