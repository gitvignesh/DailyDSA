#### **1. What is the difference between a nested class and an inner class in Kotlin?** 
- A **nested class** is **static** (doesn't hold a reference to the outer class).
- An **inner class** is **non-static** and has an implicit reference to the outer class. Use the `inner` keyword for inner classes in Kotlin.

#### **2. How does Kotlin handle references?**

Kotlin (and Java) abstracts pointers using **references**.
- A **reference** is a variable that stores the location of an object in memory, but it doesn’t allow direct manipulation of memory addresses.
- When you assign an object to a variable, the variable holds a reference to that object, not the object itself.

#### **3. In Kotlin (running on the JVM), memory is divided into two main areas:**
- **Heap Memory**: Stores objects.
- **Stack Memory**: Stores references to objects.