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
            **onCreate():** Called when the activity is first created.
            **onStart():** Called when the activity becomes visible to the user.
            **onResume():** Called when the activity starts interacting with the user.
            **onPause():** Called when the activity is partially visible and interacting with the user is paused.
            **onStop():** Called when the activity is no longer visible to the user.
            **onDestroy():** Called when the activity is being destroyed.

* **What is a Fragment, and how does it differ from an Activity?**

    **Answer:**
        A Fragment is a reusable portion of UI that can be embedded within an Activity. Unlike an Activity, a fragment cannot exist independently; it must be hosted within an activity. Fragments help in building flexible and reusable UIs, especially in larger screens like tablets.

* **What is the difference between onCreate() and onStart() in an Android Activity?**

    **Answer:**
        **onCreate()** is called when the activity is first created, and it is used for initial setup, such as inflating the UI and initializing components.
        **onStart()** is called just before the activity becomes visible to the user, typically after onCreate(). It is used to start processes that should be visible to the user but not necessarily interactive yet.

* **What are the types of Intent in Android?**

    **Answer:**
        There are two types of Intent:
            **Explicit Intent:** Used to launch a specific activity or service by specifying the exact component name.
            **Implicit Intent:** Used when the component is not specified, and Android resolves the intent to an appropriate app or component that can handle the action (e.g., sharing content or opening a web link).



## Basic Kotlin Questions

* **What is the difference between var and val in Kotlin?**

    **Answer:**
        var is used to declare a mutable variable, meaning its value can be changed.
        val is used to declare an immutable variable, meaning its value cannot be changed after it's assigned.

* **Explain nullable types in Kotlin. What is the ? operator?**

    **Answer:**
        In Kotlin, a type can be nullable by adding ? to its type. For example, String? means the variable can hold either a String value or null.
        The ? operator is used to make a type nullable, allowing safe handling of null values.

* **What are Kotlin's primary constructors and secondary constructors?**

    **Answer:**
        A primary constructor is defined in the class header and is used to initialize class properties.
        Secondary constructors are defined within the class body using the constructor keyword and are used when more complex initialization is needed.

* **What are data classes in Kotlin?**

    **Answer:**
        Data classes are classes that are used to hold data. They automatically provide useful methods like toString(), hashCode(), equals(), and copy() by default. A data class must have at least one primary constructor parameter.

* **What is a sealed class in Kotlin, and why is it useful?**

    **Answer:**
        A sealed class is a class that restricts the inheritance hierarchy. All subclasses of a sealed class must be defined in the same file. This makes it useful when representing restricted or fixed sets of types, such as in state handling or modeling success/failure outcomes.

* **What is the purpose of companion object in Kotlin?**

    **Answer:**
        companion object is used to define static members or functions in a class, similar to static members in Java. It allows you to create a single object associated with a class, giving access to properties and methods that are common to all instances of the class.
   
   

## Kotlin Coroutines

Coming soon..



## Core Java Questions

Coming soon..


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
