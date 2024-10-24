# 📘 Android & Kotlin Interview Questions & Answers

A comprehensive collection of frequently asked Android and Kotlin interview questions, with clear explanations and code examples. Ideal for both beginners and seasoned developers preparing for technical interviews. 🚀

<!--
## 📑 Table of Contents

   - 📋 [Overview](#overview)
   - 📂 [Kotlin Questions](#basic-kotlin-questions)
   - 📂 [Android Questions](#android-questions)
   - 💡 [Useful Resources](#useful-resources)
   - 🤝 Contributing
   - 📜 [License](#license)

-->

## 📋 Overview

This repository aims to help Android developers brush up on their Kotlin and Android development skills before interviews. It includes questions that cover a wide range of topics, from basic syntax to advanced concepts, ensuring you’re well-prepared to tackle any technical challenge.

  - **Purpose:** Prepare for Android/Kotlin job interviews.
  - **Difficulty Levels:** Beginner, Intermediate, Advanced.
  - **Focus Areas:** Android Core Concepts, Kotlin Programming, Jetpack Components, Coroutines, and Architecture Patterns.

<!--
## 📂 Kotlin Questions

This section includes questions ranging from core language features to advanced Kotlin concepts.

### 📝 Sample Questions

  - What are data classes in Kotlin, and what is their use?
  - Explain the difference between sealed classes and enum classes in Kotlin.
  - What is the purpose of inline functions? When should they be used?

🔗 Full Kotlin Questions List 

[View Basic Kotlin Questions](./kotlin/basic_questions.md)

## 📂 Android Questions

This section covers Android-specific topics, including lifecycle management, architecture patterns, Jetpack libraries, and modern Android development practices.

### 📝 Sample Questions

  - Describe the Fragment lifecycle and how it differs from an Activity’s lifecycle.
  - What are Android Architecture Components, and why are they used?
  - What is the difference between ViewModel and LiveData?

🔗 Full Android Questions List 

[View Android Questions](./android/core_components.md)

-->


## 📝 Contents

  - [Android Questions](#android-questions)
  - [Basic Kotlin Questions](#basic-kotlin-questions)
  - [Kotlin Coroutines](#kotlin-coroutines)
  - [Core Java](#core-java-questions)
  - [Android Unit Testing](#android-unit-testing)


## Android Questions

* **What is Android?**

	**Answer:**
	Android is an open source operating system and is mainly popular for Smartphones and Tablets. This operating system is Linux Kernel based. Using Android operating system, the developer develops the functions or programs which can perform basic as well as the advanced type of operations on the Smartphone.

* **What is Android SDK?**

	**Answer:**
	To develop a mobile application, Android developers require some tools and this requirement is satisfied by “Android SDK” which is a set of tools that are used for developing or writing apps.It has a Graphical User Interface which emulates the Android environment. This emulator acts as an actual mobile device on which the developers write their code and then debug/test the same code to check if anything is wrong.

* **What is Application?**

	**Answer:**
	The Application class in Android is the base class within an Android app that contains all other components such as activities and services. The Application class, or any subclass of the Application class, is instantiated before any other class when the process for your application/package is created.

* **Explain Android Architecture briefly.**

	**Answer:**
	Android architecture is in the form of software stack components.
	The below diagram describes the different layers in the Android architecture.
	- **Linux Kernel:** Linux Kernel is placed at the bottom of the software stack and is the foundation of the Android architecture. Using Linux kernel, Android provides a connection between the other layers of the software. It helps to develop drivers like the keypad, display, audio for device manufacture etc.
	- **Hardware Abstraction Layer (HAL):** HAL provides an interface between device drivers and API framework. It consists of library modules which are specific to the hardware component.
	- **Android Runtime:** Linux kernel provides multi-tasking execution environment so that multiple processes can execute each process runs on its own instance of Android Runtime (ART). Android has core runtime libraries like Dalvik VM specific libraries, Java Interoperability Libraries, Android Libraries and C/C++ libraries.
	- **Application Framework (Java API Framework):** The entire android functionalities are available through the API. It consists of multiple services like Activity Manager, Resource Manager, Notification Manager, etc., which form the environment in which the android application runs.
	- **Applications:** The Android application is a top layer and all types of in-built applications such as SMS, Browsers, Contact, etc are included in this top layer. It also includes third party applications which are installed by the user such as Games, etc.



<p align="center">
    <img alt="Android architecture" src="https://raw.githubusercontent.com/Gurpreets11/Android_Kotlin_Interview_Questions/master/assets/android-architecture.jpg">
</p>



* **Explain the build process in Android?**
	
	**Answer:**
	The build process in Android involves three steps
	- The first step consists of the compilation of the resources folder using the Android Asset Packaging Tool (AAPT). These are compiled into a single class file known as R.java, which only holds constants.
	- In the second step, the java source code needs to be compiled to .class files using javac, which are then converted to Dalvik bytecode using the ‘dx’ tool, which is one of the tools in the software development kit. The final output file is classes.ex.
	- In the third and final step, the Android apkbuilder is required to take all the inputs and build the Android Packaging Key (APK) file.


* **What are the different tools available in Android development? Explain their functions.**
	
	**Answer:**
	There are a variety of tools available to help Android developers:
	- **Android Software Development Kit (SDK) and Virtual Device Manager:** This tool is used to generate and handle Android Virtual Devices (AVD) and SDKs. Through the emulator in the AVD, you can specify the supported SDK version, storage in the SD card, screen resolution, and other abilities such as GPS and touch screen.
	- **The Android Emulator:** The AE is the implementation of the Android Virtual Machine, designed to run processes within a virtual device itself, which can be used on a development computer. The main use of this tool is in testing and debugging of Android applications. 
	- **Android Debug Bridge (ADB):** The ADB is a command line debugging application doled out with the SDK. It enables developers to communicate with the device, and facilitates actions such as the installation and debugging of an application.
	- **Android Asset Packaging Tool (AAPT):** The AAPT builds the ‘.apk’ distributable Android package file.


* **What is Context?**

	**Answer:**
	The Context in Android, as its name suggests, is the context of the current  state of your application or object. The context comes with services such as giving access to databases and preferences, resolving resources and much more. There are two types of context:
	- **Activity Context:** This context is attached to the lifecycle of an activity. It should be used when you are passing the context in the scope of an activity or you need the context whose lifecycle is attached to the current context.
	- **Application Context:** This context is attached to the lifecycle of an application. The application context can be used where you need a context whose lifecycle is separate from the current context or when you are passing a context beyond the scope of an activity.



* **What is an Activity in Android, and why is it important?**

    **Answer:**
	An Activity represents a single screen with a user interface in Android. It acts as an entry point for interacting with the app's UI. Activities are essential because they manage the lifecycle of the app's UI components and handle user interaction.

* **Explain the Android activity lifecycle.**

    **Answer:**
	The Android activity lifecycle defines a series of states an activity goes through, from creation to destruction. Key lifecycle methods include:
	- **onCreate():** Called when the activity is first created.
	- **onStart():** Called when the activity becomes visible to the user.
	- **onResume():** Called when the activity starts interacting with the user.
	- **onPause():** Called when the activity is partially visible and interacting with the user is paused.
	- **onStop():** Called when the activity is no longer visible to the user.
	- **onDestroy():** Called when the activity is being destroyed.
	
	 
	![Activity Lifecycle Image](/assets/activity_lifecycle.png)
	 
	[Learn Android Activity Lifecycle in detail](https://buffmycode.com/index.php/2024/10/17/activity-and-its-lifecycle-in-android/)


* **What is a Fragment, and how does it differ from an Activity?**

    **Answer:**
        A Fragment is a reusable portion of UI that can be embedded within an Activity. Unlike an Activity, a fragment cannot exist independently; it must be hosted within an activity. Fragments help in building flexible and reusable UIs, especially in larger screens like tablets.

* **What is the difference between onCreate() and onStart() in an Android Activity?**

    **Answer:**
	- **onCreate()** is called when the activity is first created, and it is used for initial setup, such as inflating the UI and initializing components.
	- **onStart()** is called just before the activity becomes visible to the user, typically after onCreate(). It is used to start processes that should be visible to the user but not necessarily interactive yet.

* **What are the types of Intent in Android?**

    **Answer:**
	There are two types of Intent:
	- **Explicit Intent:** Used to launch a specific activity or service by specifying the exact component name.
	- **Implicit Intent:** Used when the component is not specified, and Android resolves the intent to an appropriate app or component that can handle the action (e.g., sharing content or opening a web link).



## Basic Kotlin Questions

* **What is the difference between var and val in Kotlin?**

    **Answer:**
        var is used to declare a mutable variable, meaning its value can be changed.
        val is used to declare an immutable variable, meaning its value cannot be changed after it's assigned.

* **Explain nullable types in Kotlin. What is the ? operator?**

    **Answer:**<br/>In Kotlin, a type can be nullable by adding ? to its type. For example, String? means the variable can hold either a String value or null.
        The ? operator is used to make a type nullable, allowing safe handling of null values.

* **What are Kotlin's primary constructors and secondary constructors?**

    **Answer:**<br/>A primary constructor is defined in the class header and is used to initialize class properties.
        Secondary constructors are defined within the class body using the constructor keyword and are used when more complex initialization is needed.

* **What are Data Classes?**<br/>
    **Answer:**<br/>Data classes are specifically designed to hold the data. 
    In data classes, the Designers of Kotlin has overrided methods - equals(), hashcode() and toString() internally to feciliate the data holding capabilities.

    The main uses of data classes - 
    1. They can be easily copied structurally using copy() function,
    2. They can be used for destructuring declarations
    3. They also can inherit classes and interfaces

    Limitations of Data Classes:
    1. They cannot be open
    2. They cannot inherit another data class
    3. varargs cannot be used as arguments in data class as the data class internally needs to generate toString() and hashcode() method's logic.

* **If we create two data class objects with same data then are they equal?**<br/>
    **Answer:**<br/>Those two data are objects are equal structurally but not referentially. 

    Here is an example:
    ```Kotlin
        data class Person(name:String)
        //creating objects for data class
        val a = Person("Vamsi")
        val b = Person("Vamsi")
        println(a==b) // true; a normal class (without .equals() overridden) would return false in this case
        println(a===b) // false
    ```
	
* **What is a sealed class in Kotlin, and why is it useful?**

    **Answer:**<br/>Sealed classes are similar to enum classes which also has restrictive set of types allowed, except that Sealed classes can contains additional data to be propagated(which we cannot achieve with enum classes).
	All subclasses of a sealed class must be defined in the same file. This makes it useful when representing restricted or fixed sets of types, such as in state handling or modeling success/failure outcomes.

    ```Kotlin
    sealed class Result<out T: Any> {
        data class Success<out T: Any>(val data: T): Result<T>()
        data class Error(val exception: Exception): Result<Nothing>()
    }
    ```
    Sealed classes can contain any other clases like data class, pojo class, or even other sealed classes.
	
* **What is the purpose of companion object in Kotlin?**

    **Answer:**<br/>companion object is used to define static members or functions in a class, similar to static members in Java. It allows you to create a single object associated with a class, giving access to properties and methods that are common to all instances of the class.
   
* **lateinit vs lazy?**<br/>
    **Answer:** lateinit can be used for var properties where Kotlin promises the compiler that the variable will be initialized later failure of which will lead to exception.
    lazy can only be used for val properties. It will be initialized during the first call where the value will be stored in a cache so that another call to the same variable will serve the value stored in cache.

* **What are the types of equality in Kotlin?**<br>
    **Answer:** There are two types of equality in Kotlin - <br>
    **1) Referential Equality (===):** It tells whether the two references are pointing to same address or not. In Kotlin it is represented with '===', unlike in Java where it is represented with '=='.

    **2) Structural Equality (==):** Structural equality tells whether the data inside objects is equal or not.  Java is  Structural equality in Kotlin is represented by '==' where as in Java it is done by .equals() method.

    In Kotlin also we can use .equals method but it is recommended to use == because Kotlin internally converts a==b, for example, to the following code:
    ```Kotlin
        a?.equals(b) ?: (b === null)
    ```


* **What is the use of vararg keyword in Kotlin?**<br/>
    **Answer:**<br/>varargs are used to pass unlimited variables to the constructor.

    ```Kotlin
        fun sum(vararg values : Int) =  values.sum()
        assertEquals(5, sum(2,3)) // true
    ```
    Note: Only one vararg can be passed to a function. Multiple varargs leads to compilation error.

* **What are Destructuring Declarations in Kotlin?**<br/>
    **Answer:**<br/>Destructuring declarations allows us to destructure an object to various variables.

    Let us take a data class for example. We know that whenever we pass args to data class, Kotlin creates a component for each arg, named - component1(), component2() etc.

    Destructured declarations simply points to those components in the same order respectively.

    Here's an example: 
        
    ```Kotlin
        data class Person(val name: String, val age: Int)

        // destructuring declarations
        val (username, userAge) = Person("vamsi", "21")
        println(username) // vamsi
    ```
    Here these username and userAge will directly point to the component functions of data class internally as follows:
    ```Kotlin
        val username = Person.component1()
        val userAge = Person.component2()
    ```   


* **What are various scoping functions in Kotlin and when to use each of them?**<br/>
    **Answer:**<br/>There are 5 different scoping functions in Kotlin - let, apply, also, with, run. Basically they are used to execute a block of code within the context of an object.

    ***Scope Functions Table:***

    ![Scope Functions Table](/assets/scope-funcs-table.png)

    <b>1. Let:</b> <i>let</i> is an extension function that takes lambda block as parameter, has 'it' as object reference inside the block and returns the lambda block's result as return type.

    Here's the syntax of let:
    ```Kotlin
    inline fun <T, R> T.let(block: (T) -> R): R {
        return block(this)
    }
    ```
    
    Here's an example:
    ```Kotlin
    val fullName : String = Person()?.let {
        it.name = "Vamsi"
        it.name + " Tallapudi" // return value
    }
    println(fullName) //Vamsi Tallapudi
    ```
    <b>2. with:</b> <i>with</i> takes the context object and the code block (lambda) as the arguments, has 'this' as object reference inside the block and performs the lambda functions operation on the context passed. Returns the lambda result as return value.

    Here's the syntax:
    ```Kotlin
    inline fun <T, R> with(receiver: T, block: T.() -> R): R {
        return receiver.block()
    }
    ```

    Here's an example:
    ```Kotlin
    val myList = mutableListOf(1, 2, 3, 4, 5)
    val additionOfSquares = with(myList) {
        val squaresList= map { it * it }
        squaresList.sum() //returns the sum value
    }
    println(additionOfSquares) // 55
    ```

    <b>3. apply:</b> <i>apply</i> is an extension function that takes  the code block (lambda) as an argument, has 'this' as object reference inside the block and performs the lambda function on the context. Returns context object as the return value.

    Here's the syntax:
    ```Kotlin
    public inline fun <T> T.apply(block: T.() -> Unit): T {
        ...
        block()
        return this
    }
    ```
    Here's an example:

    ```Kotlin
    val vamsi = Person().apply {
        name = "Vamsi"
        age = 21
    }
    println(vamsi.age) // 21
    ```


    <b>4. also:</b> <i>also</i> is an extension function that takes  the code block (lambda) as an argument, has 'it' as object reference inside the block and performs the lambda function on the context. Returns context object as the return value.

    ```Kotlin
    val vamsi = Person().apply
    {
        name = "Vamsi"
    }.also {
        it.age = 21
    }
    println(vamsi.age) // 21
    ```

    <b>5. run:</b> <i>run</i> is an extension function that takes  the code block (lambda) as an argument, has 'this' as object reference inside the block and performs the lambda function on the context. Returns the lambda result as return value.

    ```Kotlin
    val vamsi = Person().apply
    {
        name = "Vamsi"
    }.also {
        it.age = 21
    }
    println(vamsi.age) // 21
    ```
<!--
    For more details, [Click Here.](https://medium.com/@fatihcoskun/kotlin-scoping-functions-apply-vs-with-let-also-run-816e4efb75f5)
-->

* **What are inline functions? When to use them?**<br/>
    **Answer:**<br/>Functions that take lambda parameter as arguments generates objects inside calling function's code. If these functions are called at multiple places, multiple objects are created which affects the performance of our Android App. To avoid these memory allocations created by lambda expressions (anonymous objects are created), we make the functions inline by adding a keyword - 'inline' to our function.

    ```Kotlin
    inline fun SharedPreferences.edit(commit: Boolean = false, action: SharedPreferences.Editor.() -> Unit) {
        val editor = edit()
        action(editor)
        if(commit)
            editor.commit()
        else
            editor.apply()

    }
    ```
    Inline functions are generally used when we need to pass small functions as parameters. It is generally not advisable to pass large functions to inline functions.

* **What are noinline keyword? Where we need to use them in realtime scenario?**

    **Answer:**<br/>We cannot pass a lambda function, which comes as argument inside inline function, to another function that accepts lambda. We will get an error stating 'Illegal usage of inline-parameter'. In this case we need to pass that lambda function with noinline keyword which makes the compiler instead of writing the code to the called location, creates the function for that specific function.

    Here's an example:
    ```Kotlin
    inline fun SharedPreferences.edit(
    commit: Boolean = false,
    noinline anotherFunction: Int.() -> Unit = {},
    action: SharedPreferences.Editor.() -> Unit)
    {
        // passing noinline function to another function
        myFun(anotherFunction)

        val editor = edit()
        action(editor)
        if(commit)
            editor.commit()
        else
            editor.apply()

    }

    fun myFun(importantAction: Int.() -> Unit) {
        importantAction(-1)
    }
    ```

    We'll use this only in case if multiple lambdas are passed to function arguments. If there is only one lambda which need to be referenced in another function, we better not use inline function at all.



* **What is the use of crossinline in Kotlin?**
    
    **Answer:**<br/>When we don't want to return inside lambda function (non-local returns) that is passed as inline argument, we use crossinline keyword on that lambda argument.
    
    Here's an example:
    ```Kotlin
    fun createPerson() {
        val person = Person()
        person.name = "Vamsi"
        performFunction {
            println("Created a person with name: ${person.name}")
    //        return  // Not allowed here as its crossinline
        }
    }

    inline fun performFunction (crossinline x : () -> Unit) {
        x()
    }
    ```

* **What is the use of infix in Kotlin?**

    **Answer:**<br/>infix functions are used for declaring a short form notation of a function.

    Here's an example:

    ```Kotlin
    infix fun Int.printSmallest(x: Int) {
        print(if(this < x) this else x)
    }

    1 printSmallest 5 // calling the function directly
    ```




## Kotlin Coroutines

Coming soon..



## Core Java Questions

* **What is the difference between JDK, JRE, and JVM?**

	**Answer:**
    
	**JDK (Java Development Kit):**
        It is a development environment for building applications, applets, and components using Java. It includes the JRE, compiler (javac), and other tools (like javadoc and java debugger).
        It is required for developing Java applications.

    **JRE (Java Runtime Environment):**
        It provides the libraries, JVM, and other components to run applications written in Java.
        It does not contain any development tools like compilers and debuggers.
        If you only want to run a Java program, JRE is sufficient.

    **JVM (Java Virtual Machine):**
        It is a part of JRE responsible for executing Java bytecode.
        JVM provides a platform-independent way of executing Java code, which is why Java is known as "Write Once, Run Anywhere."
        It performs several tasks like memory management (using Garbage Collection) and security checks.

* **Explain the concept of OOPs and its principles (Inheritance, Encapsulation, Polymorphism, Abstraction).**

    **Answer:**
	
	**Object-Oriented Programming (OOP):**
        It is a programming paradigm based on the concept of "objects," which can contain data (fields or attributes) and methods (functions).
        It aims to implement real-world entities like inheritance, polymorphism, and encapsulation into programming.

    **Principles of OOP:**
	
    **Inheritance:** It allows one class to inherit the properties and methods of another class. The existing class is called the parent class or superclass, and the derived class is called the child class or subclass.
        
	**Encapsulation:** It is the mechanism of wrapping the data (fields) and the methods that operate on the data into a single unit, called a class. It also restricts access to the internal state of an object using access modifiers.
        
	**Polymorphism:** It means "many forms." In Java, it allows one interface to be used for a general class of actions. The two types are compile-time polymorphism (method overloading) and runtime polymorphism (method overriding).
    
	**Abstraction:** It hides the implementation details from the user and only shows the functionality. Abstract classes and interfaces are used to achieve abstraction in Java.

* **What are the various access specifiers in Java? Explain their scope.**

	**Answer:**
	
	Java provides four access specifiers that determine the scope of a class, variable, method, or constructor:
	
	**public:**
    Visible everywhere in the project.
    It can be accessed from any class, regardless of the package.
    
	**protected:**
    Visible within the same package and subclasses in different packages.
    Often used when inheritance is involved.
    
	**default (no modifier):**
    Visible only within the same package.
    If no access specifier is specified, it is considered default.
    
	**private:**
    Visible only within the same class.
    It cannot be accessed from any other class.

* **What is the difference between == and equals() in Java?**

	**Answer:**
    
	**== Operator:**
	
    It is a reference comparison operator.
    It checks whether two references point to the same memory location.
    For primitive types, it compares the actual values.
    
	Example:
		
		String str1 = "Hello";
		String str2 = "Hello";
		System.out.println(str1 == str2); // true (because they refer to the same memory location)

	**equals() Method:**

	It is used for content comparison between objects.
	In the String class, it is overridden to compare the actual contents.
	
	Example:
		
		String str1 = new String("Hello");
		String str2 = new String("Hello");
		System.out.println(str1.equals(str2)); // true (because it compares the content)
		System.out.println(str1 == str2); // false (because they are different objects)


* **What is a constructor in Java? Explain the types of constructors.**

	**Answer:**
    
    A constructor is a special method that is called when an object is instantiated.
    It initializes the object and sets up its initial state.
    Constructors do not have a return type, not even void.
    They must have the same name as the class.
    
	**Types of Constructors:**
    
	**Default Constructor:** A no-argument constructor provided by the compiler if no constructor is defined.
    It initializes the object with default values.
    Example:
			
		class MyClass {
			MyClass() {
				System.out.println("Default constructor called");
			}
		}

	**Parameterized Constructor:** A constructor that takes one or more parameters to initialize the object with specific values.
    Example:

		class MyClass {
			int x;
			MyClass(int value) {
				this.x = value;
			}
		}



* **What is the difference between method overloading and method overriding?**

	**Answer:**

	**Method Overloading:**
	It occurs when two or more methods in the same class have the same name but different parameters (type, number, or order).
	It is a compile-time polymorphism.
	
	Example:
	
		class MyClass {
			void display(int a) {}
			void display(String b) {}
		}


	**Method Overriding:**
	It occurs when a subclass has a method with the same name, return type, and parameters as a method in its superclass.
	It is a runtime polymorphism.
	
	Example:
	
		class Parent {
			void show() {}
		}

		class Child extends Parent {
			@Override
			void show() {}
		}


* **What is an interface, and how is it different from an abstract class?**
	**Answer:**

	**Interface:**

	It is a reference type in Java, similar to a class, that can contain only abstract methods (until Java 7) and default or static methods (from Java 8).
	All fields in an interface are public, static, and final by default.
	A class implements an interface and provides implementations for its methods.
    
	**Differences from Abstract Class:**

	- Abstract Class: Can have both abstract and concrete methods, instance variables, and constructors.
	- Interface: Cannot have instance variables or constructors. Only contains abstract methods (before Java 8).
	- Multiple Inheritance: A class can implement multiple interfaces but can extend only one abstract class.

* **What is the use of the final keyword in Java?**
  **Answer:**

  The final keyword is used in different contexts:

  **final variable:**

  - Its value cannot be changed once assigned.
  - It becomes a constant.
  - Example: 
	    
		final int MAX_VALUE = 100;
    
  **final method:**
  - Cannot be overridden by subclasses.
  - Example:
		
		class Parent {
		final void show() {}
		}

  **final class:**

  - Cannot be subclassed.
  - Example:
	
		final class MyClass {}


  **final parameter:**
  - The parameter value cannot be changed inside the method.
  - Example: 

		void method(final int x) {}
		

* **Explain the difference between ArrayList and LinkedList in Java.**

  **Answer:**

  **ArrayList:**

  - Uses a dynamic array to store elements.
  - Provides faster access time (O(1)) for accessing elements by index.
  - Insertion and deletion are slower (O(n)) because elements need to be shifted.
  - Better for random access and smaller data sets.

  **LinkedList:**

  - Uses a doubly linked list to store elements.
  - Access time is slower (O(n)) as it requires traversal.
  - Insertion and deletion are faster (O(1)) as it involves adjusting pointers.
  - Better for frequent insertions and deletions.
		



* **What is a HashMap? How does it work internally?**

	**Answer:**

	**HashMap:**
	- It is a part of the Java Collections Framework and implements the Map interface.
	- It stores key-value pairs, where each key is unique.
	- Allows one null key and multiple null values.
	- Provides O(1) time complexity for get() and put() operations in the average case.

	**How HashMap Works Internally:**
	- It uses a hashing mechanism where a hash code is generated for each key.
	- The hash code determines the bucket where the key-value pair is stored.
	- If two keys have the same hash code, a collision occurs, and HashMap uses a linked list or binary tree (if the list length exceeds 8) to store multiple values in the same bucket.
	- The HashMap uses load factor (default is 0.75) to decide when to resize the internal array to maintain performance.

* **What are static methods and variables? Can we override a static method?**

	**Answer:**

	**static Variables:**
	
	- A static variable belongs to the class rather than an instance.
    - It is shared among all instances of the class.
    - Only one copy exists regardless of the number of objects created.
    - Example:
		
		  class Counter {
			static int count = 0;
			Counter() { count++; }
		  }


	**static Methods:**
	
	- A static method belongs to the class rather than any object of the class.
	- It can be called without creating an instance of the class.
	- Cannot access instance variables directly; only static variables or other static methods can be accessed.
	- Example:
	
		  class Utility {
			static void printMessage() {
				System.out.println("Hello, World!");
			}
		  }



	**Can We Override a static Method?**

	- No, static methods cannot be overridden because method overriding depends on dynamic (runtime) binding, whereas static methods are resolved at compile-time (static binding).
	- However, method hiding can occur if a subclass defines a static method with the same signature as in the parent class. The version of the method called depends on the class type used to make the call, not on the object type.
	
	
* **What is garbage collection in Java, and how does it work?**

	**Answer:**

    **Garbage Collection:**
    - It is the process of automatically freeing memory by deleting objects that are no longer reachable or needed by the program.
    - Java’s garbage collector manages the memory allocated to objects on the heap.

    **How it Works:**
	- The garbage collector identifies objects that are no longer in use (i.e., objects without any references) and deallocates the memory.
    - The process runs in the background, typically using algorithms like Mark-and-Sweep and Generational Garbage Collection.
    - Mark-and-Sweep: Identifies reachable objects (mark phase) and removes unmarked ones (sweep phase).
    - Generational Garbage Collection: Divides the heap into Young Generation and Old Generation, optimizing for short-lived objects.

* **What is the difference between throw and throws in exception handling?**

	**Answer:**

    **throw:**
    - Used to explicitly throw an exception within a method or block.
    - Can throw both checked and unchecked exceptions.
        
	- Example:
		
		  throw new IllegalArgumentException("Invalid argument");


	**throws:**

    - Used in a method signature to declare that a method can throw one or more exceptions.
    - Indicates that the calling method should handle the exception.
    - Typically used for checked exceptions.
    
	- Example:
	
		  void readFile() throws IOException {
		  // Code that may throw an IOException
		  }




* **Explain the use of synchronized keyword. How does synchronization work in Java?**

	**Answer:**

    **synchronized Keyword:**
    - Used to control access to a shared resource by multiple threads, ensuring that only one thread can access the resource at a time.
    - Helps prevent thread interference and memory consistency errors.

    **How Synchronization Works:**
    - **Method Synchronization:** Use synchronized in method signature to lock the method for a single thread.
		
		  synchronized void increment() { ... }
		
	- **Block Synchronization:** Synchronizes a specific block of code inside a method.

		  void increment() {
			synchronized (this) {
			// Code to synchronize
			}	
		  }


	- Uses a monitor lock (or intrinsic lock) associated with the object. When a thread acquires the lock, other threads cannot access synchronized code blocks of that object until the lock is released.



* **What is String, StringBuilder, and StringBuffer?**

	**Answer:**

	**`String`**:
   - A `String` in Java represents an immutable sequence of characters.
   - **Immutable** means that once a `String` object is created, its value cannot be changed.
   - Any modification, like concatenation or replacement, results in the creation of a new `String` object.
   - Stored in the **String pool**, which allows for memory optimization by reusing `String` literals.
   - Example:
     ```java
     String s = "Hello";
     s += " World"; // Creates a new String object, original "Hello" remains unchanged.
     ```

	**`StringBuilder`**:
   - A `StringBuilder` represents a mutable sequence of characters.
   - **Mutable** means that the object can be modified after it is created without creating a new object.
   - Suitable for **single-threaded environments** because its methods are not synchronized.
   - Faster than `String` and `StringBuffer` when modifications are frequent.
   - Example:
     ```java
     StringBuilder sb = new StringBuilder("Hello");
     sb.append(" World"); // Modifies the original StringBuilder object.
     ```

	**`StringBuffer`**:
   - Like `StringBuilder`, `StringBuffer` represents a mutable sequence of characters.
   - **Thread-safe** because its methods are synchronized, which means it is safe to use in **multi-threaded environments**.
   - Slower than `StringBuilder` due to the overhead of synchronization.
   - Example:
     ```java
     StringBuffer sb = new StringBuffer("Hello");
     sb.append(" World"); // Modifies the original StringBuffer object.
     ```


### Differences between `String`, `StringBuilder`, and `StringBuffer`

| **Feature**       | **String**                         | **StringBuilder**                      | **StringBuffer**                       |
|-------------------|------------------------------------|----------------------------------------|----------------------------------------|
| **Mutability**    | Immutable                          | Mutable                                | Mutable                                |
| **Thread-Safety** | Not thread-safe                    | Not thread-safe                        | Thread-safe                            |
| **Performance**   | Slower for frequent modifications  | Faster than `String` and `StringBuffer` | Slower than `StringBuilder` due to synchronization |
| **Use Case**      | When immutability is desired       | When fast performance in single-threaded context is needed | When thread safety is required in a multi-threaded context |
| **Memory Usage**  | Higher, due to creation of new objects | More efficient for modifications      | Similar to `StringBuilder`, but with overhead due to synchronization |
| **Example**       | `String s = "Hello";`              | `StringBuilder sb = new StringBuilder("Hello");` | `StringBuffer sb = new StringBuffer("Hello");` |



  **Note:**
   1. Use String when you want immutable data and are working with string literals.
   2. Use StringBuilder for mutable strings when working in a single-threaded environment where performance matters.
   3. Use StringBuffer when you need a thread-safe solution for mutable strings in multi-threaded applications.



* **How to make object thread-safe without synchronisation?**
   - **Immutable Objects**: If an object doesn’t have any mutable state, it’s inherently thread-safe. Once created, its state cannot change, so there’s no need for synchronization.
   - **Thread-Local Storage**: Use ThreadLocal variables when you need to maintain state that is unique to a thread. This way, each thread has its own instance of a variable, and no synchronization is needed.
   - **Concurrent Collections**: Utilize the concurrent collections from the java.util.concurrent package, such as ConcurrentHashMap, which are designed to handle concurrent access without explicit synchronization.
   - **Atomic Variables**: Use atomic variables from the java.util.concurrent.atomic package, like AtomicInteger or AtomicReference, which provide methods that are thread-safe without synchronization.
   - **Volatile Fields**: Declare fields as volatile to ensure that every thread sees the most recent write to the field. However, note that volatile only guarantees visibility, not atomicity.
   - **Coroutines** (Kotlin Specific): In Kotlin, you can use coroutines with shared mutable state carefully, employing mechanisms like Mutex for mutual exclusion without traditional locking.
   - **UI Thread** (Android Specific): For Android, use methods like Activity.runOnUiThread(Runnable) or View.post(Runnable) to perform actions on the UI thread safely.


* **Explain in detail Java 8 Features?**

	**Answer:**
	
	Java 8 introduced several major features that significantly enhanced the language, focusing on functional programming, improved concurrency, and ease of development. Learn java 8 features in details [from here](https://buffmycode.com/index.php/2023/05/31/java-8-features/)


## Android Unit Testing

Android Unit Testing Interview Questions and Answers:
	

Coming soon...

	

## 💡 Useful Resources

Here are some recommended resources to deepen your understanding and get hands-on experience:

  - [Official Kotlin Documentation](https://kotlinlang.org/)
  - [Android Developers Guide](https://developer.android.com/guide)
  - [Kotlin Coroutines Guide](https://kotlinlang.org/docs/coroutines-guide.html)
  - [Jetpack Compose Tutorial](https://developer.android.com/compose)
  - [Android Architecture Components](https://developer.android.com/topic/architecture)

<!-- 

## 🤝 Contributing

We welcome contributions to expand and refine the list of questions and answers. To contribute:

  1. Fork the repository.
  2. Create a new branch (feature-xyz).
  3. Add your content or make improvements.
  4. Submit a pull request.

Please ensure your submissions are well-formatted, with clear explanations and relevant code snippets where applicable.

-->

## 📜 License

This project is licensed under the MIT License - see the LICENSE file for details.

💻 Happy Coding & Best of Luck in Your Interview! 🎯
