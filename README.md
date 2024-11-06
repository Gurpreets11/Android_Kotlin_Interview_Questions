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



* **What is a Service?**<br/>
    **Answer:**
	A service is a component which doesn't have UI and can perform long running operations like downloading stuff, playing music etc.. which can run even exiting the application. By default service runs on main thread. This might cause ANR errors. To avoid this, we can Start service by creating a new background thread or use an IntentService that can do work in background. 
	[Read More.](https://developer.android.com/guide/components/services)

 
* **What are different types of services?**<br/>
    **Answer:** These are the three different types of services:

    **Foreground Service:**
    A foreground service performs some operation that is noticeable to the user. For example, an audio app would use a foreground service to play an audio track. Foreground services must display a Notification. Foreground services continue running even when the user isn't interacting with the app. <br/>
    
	**Background Service:**
    A background service performs an operation that isn't directly noticed by the user. For example, if an app used a service to compact its storage, that would usually be a background service. However there are restrictions to use background services from Android API 26 and above. We can use WorkManager to defer these background tasks.<br/>
    
	**Bound Service:**
    A service is bound when an application component binds to it by calling bindService(). A bound service offers a client-server interface that allows components to interact with the service, send requests, receive results, and even do so across processes with interprocess communication (IPC). A bound service runs only as long as another application component is bound to it. Multiple components can bind to the service at once, but when all of them unbind, the service is destroyed by the system.
    [Read More](https://developer.android.com/guide/components/services#Types-of-services)
	
	
	
* **What is a Broadcast Receiver in Android?**

	**Answer:** A Broadcast Receiver is a component that listens for system or app events and performs tasks based on those events. It is used to receive and respond to broadcast messages from other components or system events.

* **What is a Content Provider in Android?**

	**Answer:** A Content Provider is a component that manages a shared set of app data that can be accessed by other apps or components. It provides a standardized interface to access and manipulate data.



* **How do you pass data between Activities in Android?**

	**Answer:** Data can be passed between Activities in Android by using Intent extras or by using the startActivityForResult method.

* **What is the purpose of a Bundle in Android?**

	**Answer:** A Bundle is a container for data that can be passed between components in Android, such as Activities, Fragments, or Services. It is often used to save and restore instance state data.




* **What is the difference between a View and a ViewGroup in Android UI development?**
	**Answer:** In Android UI development, a View represents a UI element such as a button or a text field, while a ViewGroup is a container that holds Views and other ViewGroups. ViewGroup can hold other ViewGroups and Views, and can arrange them in different ways. For example, LinearLayout is a ViewGroup that arranges Views in a linear layout either horizontally or vertically.


* **What is the purpose of XML-based layouts in Android UI development?**

	**Answer:** XML-based layouts are used to define the structure and appearance of the user interface for an Android app. These layouts define the position, size, and style of UI elements such as buttons, text fields, and images. By defining layouts in XML, developers can separate the UI design from the app logic, making the code easier to maintain and modify.

* **How do you create a custom View in Android?**

	**Answer:** To create a custom View in Android, you need to extend the View class and override its onDraw() method to define the drawing behavior of the custom View. You can then use this custom View in your app’s XML layouts by specifying the fully-qualified name of the custom View class as the XML tag.

* **What are some common UI design principles that should be followed when developing Android apps?**

	**Answer:** Some common UI design principles that should be followed when developing Android apps include simplicity, consistency, visibility, feedback, and usability. The UI should be easy to use and understand, with clear labels and intuitive navigation. Feedback should be provided to the user when actions are performed, and consistency should be maintained across the app’s UI.

* **How do you implement a responsive design in Android UI development?**

	**Answer:** To implement a responsive design in Android UI development, you can use techniques such as RelativeLayout, ConstraintLayout, or the new GridLayout. These layout managers allow you to define UI elements in relation to each other, ensuring that the UI scales properly across different screen sizes and orientations.

* **How do you handle different screen densities in Android UI development?**

	**Answer:** In Android UI development, you can use resource qualifiers such as -hdpi, -xhdpi, and -xxhdpi to specify different versions of UI elements for different screen densities. The system will automatically load the appropriate version of the resource based on the device’s screen density.

* **What is a RecyclerView in Android UI development?**

	**Answer:** A RecyclerView is a more flexible and efficient replacement for ListView and GridView in Android UI development. It allows developers to display large sets of data in a scrollable list or grid, with customizable item views and a more efficient data loading and recycling mechanism.

* **How do you implement animations in Android UI development?**

	**Answer:** In Android UI development, you can use the Animation and Animator classes to implement animations such as fade-in, fade-out, and slide-in. You can also use the new Transition framework to create more complex animations that involve multiple UI elements.


* **What is a Material Design guideline in Android UI development?**

	**Answer:** Material Design is a set of guidelines for Android UI design created by Google. It provides a consistent and intuitive design language for Android apps, with guidelines for typography, color, layout, and animation. Adhering to Material Design guidelines can help developers create more visually appealing and user-friendly apps.

* **What is the purpose of the “match_parent” attribute in Android XML layouts?**

	**Answer:** The “match_parent” attribute is used to instruct the View to take up as much space as possible within its parent container. It is often used to create full-screen or dynamically-sized UI components.

  ```
  <TextView 
  android:layout_width="match_parent" 
  android:layout_height="wrap_content" 
  android:text="This text will take up the full width of its parent"/>
  ```

* **What are some common UI design principles for mobile apps?**
	**Answer:** Some common UI design principles for mobile apps include simplicity, consistency, feedback, affordance, and discoverability. These principles help ensure that apps are easy to use, intuitive, and visually appealing.

	**Example:**

	- **Simplicity:** An app should have a simple and straightforward UI that is easy to navigate and use.

	- **Consistency:** An app should have a consistent design language throughout its various screens and components.

	- **Feedback:** The app should provide clear feedback to users when they interact with UI components, such as buttons or text inputs.

	- **Affordance:** UI components should provide visual cues that indicate their intended function, such as a button that looks like it can be pressed.

	- **Discoverability:** All UI components should be easy to discover and accessible to users.

* **How can you improve the performance of an Android app’s UI?** 

	**Answer:** You can improve the performance of an Android app’s UI by reducing the number of layout hierarchies, minimizing the use of expensive graphics, using RecyclerView instead of ListView for long lists, and optimizing animations and transitions.

	**Example:**

	- Use a RelativeLayout instead of a nested LinearLayout hierarchy to reduce the number of layout passes required.
	- Use vector drawables instead of bitmap images to reduce the memory footprint of graphics.
	- Use the RecyclerView widget instead of the ListView widget for long lists to improve scrolling performance.
	- Use the Lint tool to detect and fix UI performance issues.

* **What is the purpose of the “dp” (density-independent pixel) unit in Android?**

	**Answer:** The “dp” unit is used to specify dimensions in a way that is independent of the device’s screen density. This allows UI components to look the same across devices with different screen densities.


  ```<Button 
  android:layout_width="100dp" 
  android:layout_height="50dp" 
  android:text="Click me!" />
  ```
	
	
* **What is the purpose of a ViewStub in Android?**

	**Answer:** A ViewStub is a lightweight UI component that allows you to defer the inflation of a UI component until it is needed. This can improve app startup times and reduce memory usage.

  ```<ViewStub 
  android:id="@+id/stub" 
  android:inflatedId="@+id/my_view" 
  android:layout="@layout/my_layout" 
  android:layout_width="match_parent" 
  android:layout_height="wrap_content" />
  ```

	In this example, the ViewStub is set up to inflate the “my_layout” layout file when it is needed. The inflated layout will have the ID “my_view”.

* **How do you handle different screen sizes in Android?**

	**Answer:** You can handle different screen sizes in Android by using layout qualifiers such as “layout-small”, “layout-large”, and “layout-xlarge” to provide different versions of your layout files for different screen sizes. You can also use the “dp” unit to specify dimensions in a way that is independent of the device’s screen density.

  ```
  res/ layout/ main.xml 
  res/ layout-small/ main.xml 
  res/ layout-large/ main.xml 
  res/ layout-xlarge/ main.xml
  ```




### Android App Architecture

* **What is Model-View-ViewModel (MVVM) architecture and how does it differ from other architectures?**

	**Answer:** MVVM is a popular architecture pattern for Android apps that separates the app into three distinct components: Model, View, and ViewModel. The Model component represents the data and business logic, the View component represents the UI, and the ViewModel acts as a mediator between the Model and View components. The key advantage of MVVM is that it makes it easier to test each component separately and enables data binding. In contrast, Model-View-Presenter (MVP) separates the View and Presenter components, while Clean Architecture uses layers to separate business logic from the presentation layer.

* **How do you implement the MVVM architecture in an Android app using Jetpack?**

	**Answer:** To implement MVVM architecture using Jetpack, you can use the following components:

	- **LiveData:** A lifecycle-aware observable data holder that can be used to communicate changes between the ViewModel and View components.
	- **ViewModel:** A class that stores and manages UI-related data, communicates with the Model component, and survives configuration changes.
	- **DataBinding:** A library that enables UI components to bind to data sources in the ViewModel and eliminates the need for findViewById() calls. You can also use other Jetpack components such as Room for database operations, Navigation for navigating between screens, and WorkManager for background processing.

* **What is dependency injection and how does it improve app architecture?**

	**Answer:** Dependency injection is a technique for managing dependencies between objects in an app. Instead of creating objects directly, you use a dependency injection framework such as Dagger to provide the required objects. This makes the app more modular, testable, and maintainable, as each component can be easily replaced or modified without affecting the rest of the app. It also reduces code duplication and improves code readability.

* **What is the role of Dagger in app architecture and how does it work?**

	**Answer:** Dagger is a popular dependency injection framework for Android that simplifies the process of managing dependencies in an app. It uses annotations to generate code that provides dependencies to other classes, eliminating the need for manual dependency injection. The main advantage of Dagger is that it enables modular app design and makes it easier to test components in isolation. It works by creating a graph of dependencies at compile time, and then using that graph to provide dependencies to the app at runtime.

* **How does the ViewModel component in Jetpack improve app architecture?**

	**Answer:** The ViewModel component in Jetpack is designed to store and manage UI-related data, such as the state of the UI and user input. It survives configuration changes, such as screen rotations, by using a lifecycle-aware mechanism that retains its state. This reduces the need for workarounds such as saving state to a Bundle, and makes it easier to separate the presentation layer from the data layer. It also enables sharing of data between multiple UI components, such as Fragments, and promotes a more modular app architecture.

* **What is the role of LiveData in Jetpack and how does it enable reactive programming?**

	**Answer:** LiveData is a lifecycle-aware observable data holder that can be used to communicate changes between the ViewModel and View components in an Android app. It enables reactive programming by allowing the View to observe changes in the ViewModel’s data, and update the UI accordingly. This eliminates the need for manual UI updates, reduces boilerplate code, and improves performance. LiveData also respects the lifecycle of the app components, such as Fragments and Activities, and automatically removes observers when they are no longer needed, preventing memory leaks.

* **Can you explain the differences between the Model-View-Controller (MVC) and Model-View-Presenter (MVP) patterns in Android app development?**

	**Answer:** The MVC pattern separates the app into three components: the model (data and business logic), the view (user interface), and the controller (mediator between the model and the view). The MVP pattern builds on the MVC pattern by adding a presenter that acts as an intermediary between the view and the model, handling user input and updating the view accordingly. In MVP, the view and the model are decoupled, making it easier to test the app.

* **How does the Model-View-ViewModel (MVVM) pattern differ from the Model-View-Presenter (MVP) pattern in Android development?**

	**Answer:** In MVVM, the view is bound to a ViewModel, which handles the presentation logic and state management. The ViewModel is responsible for retrieving and preparing data for the view to display. This pattern allows for better separation of concerns and makes it easier to test the code. Unlike in MVP, the view and the ViewModel are not coupled directly.

* **Can you explain the benefits of using the Clean Architecture pattern in Android app development?**

	**Answer:** The Clean Architecture pattern promotes separation of concerns and isolation of business logic from the framework and infrastructure layers. This makes the app more maintainable, testable, and scalable. The pattern consists of several layers, including domain, use cases, and data layers.

* **How does the use of LiveData in Jetpack improve app architecture in Android development?**

	**Answer:** LiveData is a Jetpack component that provides observable data to the UI layer. It allows for more efficient and responsive updates to the UI by automatically updating the view when the data changes. LiveData also helps to decouple the view from the business logic, making the app more maintainable.

* **Can you explain the purpose of ViewModel in Jetpack and how it relates to the UI layer in Android development?**

	**Answer:** ViewModel is a Jetpack component that provides a lifecycle-aware container for the UI-related data. ViewModel holds data for the UI, and it survives configuration changes. It keeps the data separate from the UI and provides a clean separation of concerns between the UI and data layers.

* **How does the use of Dagger in Android app development improve app architecture?**

	**Answer:** Dagger is a dependency injection framework that simplifies the management of dependencies in the app. It helps to decouple the components of the app and allows for easier testing and maintenance. It also helps to avoid boilerplate code and increases code reuse.

* **Can you explain how the Repository pattern works in Android app development?**

	**Answer:** The Repository pattern is used to manage data from different sources (such as a local database or a remote API) in a single place. The repository mediates between the data sources and the app, providing a layer of abstraction and making it easier to swap out data sources without affecting the rest of the app.

* **Can you explain how the Dependency Inversion Principle (DIP) is implemented in Android app development?**

	**Answer:** The Dependency Inversion Principle states that high-level modules should not depend on low-level modules. Instead, both should depend on abstractions. In Android app development, this means that the code should be written in a way that the business logic does not depend on the implementation details of the framework or infrastructure.



## Basic Kotlin Questions

* **What is the difference between var and val in Kotlin?**

    **Answer:**
	- var is used to declare a mutable variable, meaning its value can be changed.
    - val is used to declare an immutable variable, meaning its value cannot be changed after it's assigned.

* **Explain nullable types in Kotlin. What is the ? operator?**

    **Answer:**<br/>In Kotlin, a type can be nullable by adding ? to its type. For example, String? means the variable can hold either a String value or null.<br/>
    The ? operator is used to make a type nullable, allowing safe handling of null values.

* **What are Kotlin's primary constructors and secondary constructors?**

    **Answer:**<br/>A primary constructor is defined in the class header and is used to initialize class properties.<br/>
    Secondary constructors are defined within the class body using the constructor keyword and are used when more complex initialization is needed.

* **What is the difference between a class and an object in Kotlin?**

	**Answer:**<br/>A class is a blueprint for creating objects, while an object is a single instance of a class. Objects are often used to implement singletons in Kotlin.


* **What are Data Classes?**<br/>
    **Answer:**<br/>Data classes are specifically designed to hold the data. 
    In data classes, the Designers of Kotlin has overrided methods - **equals()**, **hashcode()** and **toString()** internally to feciliate the data holding capabilities.

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
    **Answer:**<br/>lateinit can be used for var properties where Kotlin promises the compiler that the variable will be initialized later failure of which will lead to exception.
    lazy can only be used for val properties. It will be initialized during the first call where the value will be stored in a cache so that another call to the same variable will serve the value stored in cache.

* **What are the types of equality in Kotlin?**<br>
    **Answer:**<br/>There are two types of equality in Kotlin - <br>
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



* **What is a lambda expression in Kotlin?**

	**Answer:** <br/>A lambda expression is a way to define a function in Kotlin without creating a separate named function. It allows you to define a function inline, using a more concise syntax. For example, the following code defines a lambda expression that takes two integers and returns their sum: “(x: Int, y: Int) -> x + y”.

* **What is the difference between a lateinit property and an initialized property in Kotlin?**

	**Answer:** <br/>A lateinit property is a property that is declared without an initial value, but is guaranteed to be initialized before it is used. This is useful for properties that cannot be initialized in the constructor, but need to be initialized before they are used. An initialized property, on the other hand, is a property that is declared with an initial value and can be used immediately.



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




## Kotlin Coroutines

Coming soon..


## Advance Question

* **What is Retrofit and how does it work?**

* **What is the difference between Gson and Jackson libraries for JSON parsing in Android?**

* **What is Room and how is it used for data persistence in Android?**

* **What is the difference between synchronous and asynchronous network requests in Android?**


* **What is Retrofit in Android? How does it work?**

* **What is Room in Android? How is it different from SQLite?**

* **What is the difference between REST and SOAP APIs?**

* **How do you handle network requests in Android?**

* **What is Okhttp?**

* **What is the purpose of the Cache-Control header in HTTP requests?**

* **What is JSON? How is it used in Android app development?**

<!--   
Reference:
 
https://medium.com/@vikasacsoni9211/quest-for-android-excellence-interview-edition-2024-part-i-11d5c517e9f6

-->


## Multithreading and Concurrency

What is the difference between a process and a thread in Android?


What are the different ways to implement multithreading in Android?

What is the difference between AsyncTask and Thread in Android?

What is synchronization in Android, and why is it important?

What is a deadlock in multithreading, and how can it be prevented?

What is a Handler in Android, and how does it work?

What is a race condition in multithreading, and how can it be prevented?

What is the difference between a synchronous and asynchronous operation in Android?

What is a ThreadPoolExecutor in Android, and how does it work?

What is the role of a ContentProvider in Android, and how is it related to multithreading?




## Performance Optimization

What are the different types of performance issues you have encountered in Android apps? How did you identify and resolve them?



What is the difference between using ListView and RecyclerView for displaying large sets of data in an Android app? When would you choose one over the other?


What is the purpose of using a cache in an Android app? What are some strategies you can use to implement a cache?


How do you handle memory leaks in an Android app? What tools can you use to detect and fix memory leaks?

Can you explain what caching is and how it can be used to improve the performance of an Android app?


What is memory management in Android, and how can it be optimized for better performance?

What is performance profiling in Android, and how can it be used to identify performance bottlenecks?

How can you optimize the rendering of UI elements in an Android app?

Can you explain the difference between synchronous and asynchronous network requests, and when would you use each one?


How can you implement background tasks in an Android app, and what are the best practices for doing so?

Can you explain the difference between a bitmap and a drawable, and when would you use each one?


How can you use the RecyclerView to improve the performance of a list in an Android app?


 

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
