## 📘 Kotlin Interview Questions & Answers

**1. What is the difference between var and val in Kotlin?**

  **Answer:**
     var is used to declare a mutable variable, meaning its value can be changed.
     val is used to declare an immutable variable, meaning its value cannot be changed after it's assigned.

**2. Explain nullable types in Kotlin. What is the ? operator?**

  **Answer:**
     In Kotlin, a type can be nullable by adding ? to its type. For example, String? means the variable can hold either a String value or null.
     The ? operator is used to make a type nullable, allowing safe handling of null values.

**3. What are Kotlin's primary constructors and secondary constructors?**

  **Answer:**
     A primary constructor is defined in the class header and is used to initialize class properties.
     Secondary constructors are defined within the class body using the constructor keyword and are used when more complex initialization is needed.

**4. What are data classes in Kotlin?**

  **Answer:**
     Data classes are classes that are used to hold data. They automatically provide useful methods like toString(), hashCode(), equals(), and copy() by default. A data class must have at least one primary constructor parameter.

**5. What is a sealed class in Kotlin, and why is it useful?**

   **Answer:**
     A sealed class is a class that restricts the inheritance hierarchy. All subclasses of a sealed class must be defined in the same file. This makes it useful when representing restricted or fixed sets of types, such as in state handling or modeling success/failure outcomes.

**6. What is the purpose of companion object in Kotlin?**

   **Answer:**
     companion object is used to define static members or functions in a class, similar to static members in Java. It allows you to create a single object associated with a class, giving access to properties and methods that are common to all instances of the class.


   
