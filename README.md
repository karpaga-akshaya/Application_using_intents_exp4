# Application_using_intents_exp4
The application demonstrates navigation from a Login Activity to a Home Activity and also shows how data can be transferred between activities using Intent extras.

## 1. Experiment Title

**Develop an application to link activities using Intents.**

## 2. Objective

The objective of this experiment is to develop an Android application that demonstrates how two activities can be linked using an Intent.

The application demonstrates navigation from a Login Activity to a Home Activity and also shows how data can be transferred between activities using Intent extras.

## 3. Concept Used

### Intent

An Intent is a messaging object provided by Android that is used to request an action from another Android component.

In this experiment, an **Explicit Intent** is used because the application knows exactly which activity should be opened.

Example:

```kotlin
val intent = Intent(this, HomeActivity::class.java)
startActivity(intent)
```

The above statement starts `HomeActivity` from `LoginActivity`.

## 4. Scenario

A simple login application is developed using two activities.

### Activity 1 – LoginActivity

The first activity contains:

* Username field
* Password field
* Login button

When the user enters the required details and clicks the Login button, an Explicit Intent is created to navigate to the second activity.

### Activity 2 – HomeActivity

The second activity displays a welcome message containing the username received from the Login Activity.

## 5. Data Transfer Between Activities

The username is transferred from one activity to another using `putExtra()`.

```kotlin
intent.putExtra("USERNAME", user)
```

The value is retrieved in the second activity using:

```kotlin
val username = intent.getStringExtra("USERNAME")
```

Therefore, the experiment demonstrates both:

1. Activity navigation using Intent.
2. Data transfer using Intent extras.

## 6. Technologies Used

* Android Studio
* Kotlin
* XML
* Android SDK
* Explicit Intent
* Android Activity

## 7. Project Structure

```text
IntentActivityLinking/
│
├── app/
│   └── src/
│       └── main/
│           ├── java/
│           │   └── com.example.intentactivitylinking/
│           │       ├── LoginActivity.kt
│           │       └── HomeActivity.kt
│           │
│           ├── res/
│           │   ├── drawable/
│           │   ├── layout/
│           │   │   ├── activity_login.xml
│           │   │   └── activity_home.xml
│           │   └── values/
│           │       ├── colors.xml
│           │       ├── strings.xml
│           │       └── themes.xml
│           │
│           └── AndroidManifest.xml
│
├── build.gradle.kts
├── settings.gradle.kts
└── README.md
```

## 8. Important Files

| File                  | Description                                               |
| --------------------- | --------------------------------------------------------- |
| `LoginActivity.kt`    | Controls the Login Activity and creates the Intent        |
| `HomeActivity.kt`     | Receives the Intent data and displays the welcome message |
| `activity_login.xml`  | Defines the Login Activity user interface                 |
| `activity_home.xml`   | Defines the Home Activity user interface                  |
| `AndroidManifest.xml` | Registers both activities                                 |
| `README.md`           | Contains project documentation                            |

## 9. Application Flow

```text
Start Application
       ↓
LoginActivity
       ↓
Enter Username and Password
       ↓
Click Login
       ↓
Create Explicit Intent
       ↓
Pass Username using putExtra()
       ↓
startActivity()
       ↓
HomeActivity
       ↓
Display Welcome Message
```

## 10. Result

The Android application successfully links two activities using an Explicit Intent. The application navigates from the Login Activity to the Home Activity and transfers the entered username between the activities.

## 11. Conclusion

Thus, the application successfully demonstrates activity navigation using Intents in Android. It also demonstrates how data can be passed from one activity to another using Intent extras.
