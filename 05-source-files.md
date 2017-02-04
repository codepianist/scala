# Scala:

### Files and Packages:
- Files are very flexible, can contain almost anything:
    - Order.scala does not have to contain a class named Order.
- Packages does not have to have the same name of the folder.
- There's no protective keyword like in Java: private, protected, public.
    - Packaged objects: 
        - Code that you can use within package scope
        - You can import a class or the entire package
- Imports can be renamed, you can create an alias.
- Type aliases: to help to clarify a complex type (Similar to hash define macro in C, or type synonyms in Haskel).
- Don't have interfaces, have traits (can have methods): Something between Java 8 default methods and Ruby Mixins.