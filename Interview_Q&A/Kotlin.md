#### 1. What is the difference between a nested class and an inner class in Kotlin?
- A **nested class** is **static** (doesn't hold a reference to the outer class).
- An **inner class** is **non-static** and has an implicit reference to the outer class. Use the `inner` keyword for inner classes in Kotlin.
#### 2. How does Kotlin handle references?
Kotlin (and Java) abstracts pointers using **references**.
- A **reference** is a variable that stores the location of an object in memory, but it doesn’t allow direct manipulation of memory addresses.
- When you assign an object to a variable, the variable holds a reference to that object, not the object itself.
#### 3. In Kotlin (running on the JVM), memory is divided into two main areas:
- **Heap Memory**: Stores objects.
- **Stack Memory**: Stores references to objects.
#### 4. What are higher order functions in kotlin
A **higher-order function** is a function that either:
1. Takes another function as a parameter, or
2. Returns a function as its result.

Benefits of Higher-Order Functions
1. **Code Reusability**: Avoid repetitive logic.
2. **Expressiveness**: Makes code easier to read and understand.
3. **Functional Programming**: Encourages immutability and declarative code.

#### 5. What is the difference between: What is the difference between inline, noinline, and crossinline in Kotlin:

|Keyword|Behavior|
|---|---|
|`inline`|Inlines the function and lambdas to reduce overhead; allows non-local returns unless `crossinline`.|
|`noinline`|Prevents specific lambdas from being inlined within an `inline` function.|
|`crossinline`|Prevents non-local returns from lambdas in `inline` functions to maintain predictable control flow.|
#### 6. What are the key features of Kotlin?
Conciseness: Reduced boilerplate code.
Null Safety: Eliminates `NullPointerExceptions` with nullable and non-nullable types.
Interoperability: Fully interoperable with Java.
Extension Functions: Add functionality to existing classes.
Coroutines: Simplify asynchronous programming.
Type Inference: Reduces explicit type declaration.
#### 7. What is the difference between `apply`, `let`, `run`, `also`, and `with`?
- `apply`: Used for configuring an object and returns the object itself.
- `let`: Executes a block with `it` as the receiver, returns the block's result.
- `run`: Executes a block and returns the result; uses `this` as the receiver.
- `also`: Like `apply`, but `it` is the receiver and returns the object.
- `with`: Used for calling methods on an object without returning it.

#### 8. What is the difference between fun and inline fun ?
- `fun`: Normal function.
- `inline fun`: Requests the compiler to copy the function's body to the call site, reducing overhead of higher-order functions.

#### 9. What is the `lazy` keyword in Kotlin? ####
`lazy` is used to initialize properties only when accessed for the first time.

#### 10. What is the purpose of the `@JvmStatic` and `@JvmOverloads` annotations?
- `@JvmStatic`: Makes a method callable as a static method in Java.
- `@JvmOverloads`: Generates multiple overloads for functions with default parameters.

#### 11. What is the difference between `Array` and `List` in Kotlin?
- `Array`: Fixed-size, mutable collection of elements.
- `List`: Immutable by default, supports both mutable (`MutableList`) and immutable (`List`) versions.
#### 12. What is the difference between `HashMap` and `MutableMap` in Kotlin?
- `HashMap`: Implementation of `MutableMap` backed by a hash table.
- `MutableMap`: Generic interface for mutable maps.

#### 13. What is the difference between `filter`, `map`, and `flatMap` in Kotlin?
- `filter`: Filters elements based on a predicate.
- `map`: Transforms elements.
- `flatMap`: Transforms and flattens nested collections.

#### 14. What are coroutines builders in Kotlin?
- Builders like `launch` and `async` create coroutines.
- `launch`: Does not return a value.
- `async`: Returns a `Deferred` that provides a result.

#### 15. What are `in` and `out` keywords in Kotlin generics?
- `in`: Defines a contravariant type (input type).
- `out`: Defines a covariant type (output type).

#### 16. What are type aliases in Kotlin?
Type aliases provide alternate names for existing types, improving readability.

