## 1. Main Thread, Looper, Message Queue
## 2. Gradle
## 3. Manifest

## 4. Android Components (Entry Points)


**Topics to explore:**
1. What does a "Class" actually mean ? like referring the class using: "::"

---
### 1. Activities

**Launch Modes**
1. Standard: Normal mode without checking any stack.
2. Single Top: If there is an instance at the **_Top_** of the stack then do not create else create new.
3. Single Task: If there is an instance already in the stack then do not create and **_pop the stack till the instance_** else create new.
4. Single Instance: Create a new task stack and create and add the new instance.



___
### 2. Services

---
### 3. Broadcast Receivers 

---
### 4. Intents

An **Intent** in Android is a messaging object that allows components (such as activities, services, and broadcast receivers) to communicate with each other. Types of intents:
A. Explicit Intent
B. Implicit Intent

Operations Related to intents: 
I. Intent Filters
II. Intent Flags

#### A. Explicit Intent
Used to start a specific component within the same application or another application where the component is known.
```kotlin
val intent = Intent(this, SecondActivity::class.java)
intent.putExtra("message", "Hello from MainActivity!") 

startActivity(intent)
```

#### B. Implicit Intent
Used when you don’t specify the exact component but instead declare an action to be performed. The system determines the appropriate component to handle the request.
```kotlin
val intent = Intent(Intent.ACTION_VIEW) 
intent.data = Uri.parse("https://www.google.com") 

startActivity(intent)
```

### I. Intent Filters
**Intent filters** are required when you want your app to handle **implicit intents**—those where the calling component does not specify a specific target component (like an activity, service, or broadcast receiver)

Example:
```xml
<activity android:name=".WebActivity"> 
	<intent-filter>
		<action android:name="android.intent.action.VIEW"/> 
		<category android:name="android.intent.category.DEFAULT"/>
		<category android:name="android.intent.category.BROWSABLE"/> 
		<data android:scheme="https" android:host="www.example.com"/>
	</intent-filter> 
</activity>
```

### II. Intent Flags
Flags modify how activities are launched. Some common ones:
- `FLAG_ACTIVITY_NEW_TASK` – Starts a new task.
- `FLAG_ACTIVITY_CLEAR_TOP` – Clears all activities above the target one.
- `FLAG_ACTIVITY_SINGLE_TOP` – Reuses an existing instance of the activity.

---

