### 1. What is difference between Explicit and Implicit filter ?

| Feature                 | Explicit Intent                            | Implicit Intent                                      |
| ----------------------- | ------------------------------------------ | ---------------------------------------------------- |
| **Component Targeting** | Targets a specific component directly      | Targets a general action, no specific component      |
| **Usage Scope**         | For internal communication within your app | For interacting with other apps or system components |
| **Intent Filter**       | Not required in the target component       | Required in the receiving components                 |
| **Examples**            | Navigating between activities or services  | Opening a web page, sharing content                  |
Explicit code:
```kotlin
val intent = Intent(this, TargetActivity::class.java) 
startActivity(intent)
```

Implicit code:
```kotlin
val intent = Intent(Intent.ACTION_VIEW).apply { 
	data = Uri.parse("https://www.example.com")
} 
startActivity(intent)
```
### 2. What is the purpose of ViewModel in Android? How does it retain data during configuration changes?

1. What is the difference between Compose "State" and Coroutine "StateFlow" ? 
   When to use what?
2. What is the difference between update methods for StateFlow ?
3. What is remember and derivedStateOf ? when to use what ?
4. what are scope functions in kotlin? explain its use case?
   
   