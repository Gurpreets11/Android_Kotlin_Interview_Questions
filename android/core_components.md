 ## 📘 Android Interview Questions & Answers

**1. What is an Activity in Android, and why is it important?**

Answer:
      An Activity represents a single screen with a user interface in Android. It acts as an entry point for interacting with the app's UI. Activities are essential because they manage the lifecycle of the app's UI components and handle user interaction.

**2. Explain the Android activity lifecycle.**

Answer:
     The Android activity lifecycle defines a series of states an activity goes through, from creation to destruction. Key lifecycle methods include:
     - onCreate(): Called when the activity is first created.
     - onStart(): Called when the activity becomes visible to the user.
     - onResume(): Called when the activity starts interacting with the user.
     - onPause(): Called when the activity is partially visible and interacting with the user is paused.
      - onStop(): Called when the activity is no longer visible to the user.
      - onDestroy(): Called when the activity is being destroyed.

3. What is a Fragment, and how does it differ from an Activity?

    Answer:
        A Fragment is a reusable portion of UI that can be embedded within an Activity. Unlike an Activity, a fragment cannot exist independently; it must be hosted within an activity. Fragments help in building flexible and reusable UIs, especially in larger screens like tablets.

4. What is the difference between onCreate() and onStart() in an Android Activity?

    Answer:
        onCreate() is called when the activity is first created, and it is used for initial setup, such as inflating the UI and initializing components.
        onStart() is called just before the activity becomes visible to the user, typically after onCreate(). It is used to start processes that should be visible to the user but not necessarily interactive yet.

5. What are the types of Intent in Android?

    Answer:
        There are two types of Intent:
            Explicit Intent: Used to launch a specific activity or service by specifying the exact component name.
            Implicit Intent: Used when the component is not specified, and Android resolves the intent to an appropriate app or component that can handle the action (e.g., sharing content or opening a web link).
