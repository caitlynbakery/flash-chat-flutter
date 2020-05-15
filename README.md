# Flash Chat ⚡️

## Our Goal

The objective of this tutorial is to learn how to incorporate Firebase into our Flutter apps. We'll be using Firebase Cloud Firestore as well as the Firebase authentication package to equip our app with a cloud-based NoSQL database and secure authentication methods. 


## What you will create

We’re going to build a modern messaging app where users can sign up and log in to chat.


## What you will learn

- How to incorporate Firebase into your Flutter projects.
- How to use Firebase authentication to register and sign in users.
- How to create beautiful animations using the Flutter Hero widget.
- How to create custom aniamtions using Flutter's animation controller. 
- Learn all about mixins and how they differ from superclasses.
- Learn about Streams and how they work.
- Learn to use ListViews to build scrolling views.
- How to use Firebase Cloud Firestore to store and retrieve data on the fly.

---
---

# Named Routes
I used [named routes](https://flutter.dev/docs/cookbook/navigation/named-routes) to navigate between screens with the `Navigator` function. The first step is to define the routes in the `main.dart` file using a map called `routes`. I also changed the `home` property to `initialRoute`.

```dart
initialRoute: WelcomeScreen.id,
routes: {
    WelcomeScreen.id : (context) => WelcomeScreen(),
    LoginScreen.id: (context) => LoginScreen()
}
```

The second step is to navigate to the second screen using `Navigator.pushNamed()` when the button is pressed.

```dart
 onPressed: () {
    Navigator.pushNamed(context, RegistrationScreen.id);
    },
```
# Static Const

The static keyword is used to hold variables or methods inside a class so that you can access it without creating a new object. When a variable is static, you just need to put the class name in front of the variable when you want to use it. 

```dart
// welcome_screen.dart
static const String id = 'welcome_screen';

// main.dart
initialRoute: WelcomeScreen.id,
```