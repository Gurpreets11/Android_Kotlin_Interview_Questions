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

  - Purpose: Prepare for Android/Kotlin job interviews.
  - Difficulty Levels: Beginner, Intermediate, Advanced.
  - Focus Areas: Android Core Concepts, Kotlin Programming, Jetpack Components, Coroutines, and Architecture Patterns.

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


* **What is an Activity in Android, and why is it important?**

    Answer:
        An Activity represents a single screen with a user interface in Android. It acts as an entry point for interacting with the app's UI. Activities are essential because they manage the lifecycle of the app's UI components and handle user interaction.

* **Explain the Android activity lifecycle.**

    Answer:
        The Android activity lifecycle defines a series of states an activity goes through, from creation to destruction. Key lifecycle methods include:
            onCreate(): Called when the activity is first created.
            onStart(): Called when the activity becomes visible to the user.
            onResume(): Called when the activity starts interacting with the user.
            onPause(): Called when the activity is partially visible and interacting with the user is paused.
            onStop(): Called when the activity is no longer visible to the user.
            onDestroy(): Called when the activity is being destroyed.

* **What is a Fragment, and how does it differ from an Activity?**

    Answer:
        A Fragment is a reusable portion of UI that can be embedded within an Activity. Unlike an Activity, a fragment cannot exist independently; it must be hosted within an activity. Fragments help in building flexible and reusable UIs, especially in larger screens like tablets.

* **What is the difference between onCreate() and onStart() in an Android Activity?**

    Answer:
        onCreate() is called when the activity is first created, and it is used for initial setup, such as inflating the UI and initializing components.
        onStart() is called just before the activity becomes visible to the user, typically after onCreate(). It is used to start processes that should be visible to the user but not necessarily interactive yet.

* **What are the types of Intent in Android?**

    Answer:
        There are two types of Intent:
            Explicit Intent: Used to launch a specific activity or service by specifying the exact component name.
            Implicit Intent: Used when the component is not specified, and Android resolves the intent to an appropriate app or component that can handle the action (e.g., sharing content or opening a web link).



## Basic Kotlin Questions

* **What is the difference between var and val in Kotlin?**

    Answer:
        var is used to declare a mutable variable, meaning its value can be changed.
        val is used to declare an immutable variable, meaning its value cannot be changed after it's assigned.

* **Explain nullable types in Kotlin. What is the ? operator?**

    Answer:
        In Kotlin, a type can be nullable by adding ? to its type. For example, String? means the variable can hold either a String value or null.
        The ? operator is used to make a type nullable, allowing safe handling of null values.

* **What are Kotlin's primary constructors and secondary constructors?**

    Answer:
        A primary constructor is defined in the class header and is used to initialize class properties.
        Secondary constructors are defined within the class body using the constructor keyword and are used when more complex initialization is needed.

* **What are data classes in Kotlin?**

    Answer:
        Data classes are classes that are used to hold data. They automatically provide useful methods like toString(), hashCode(), equals(), and copy() by default. A data class must have at least one primary constructor parameter.

* **What is a sealed class in Kotlin, and why is it useful?**

    Answer:
        A sealed class is a class that restricts the inheritance hierarchy. All subclasses of a sealed class must be defined in the same file. This makes it useful when representing restricted or fixed sets of types, such as in state handling or modeling success/failure outcomes.

* **What is the purpose of companion object in Kotlin?**

    Answer:
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
