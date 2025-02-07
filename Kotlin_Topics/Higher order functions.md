Functions are first-class citizens in kotlin we can store functions same as objects.

A function taking in another function as a parameter or returning a function as a return value is called a higher order function.

|Feature|Description|
|---|---|
|Takes function as parameter|Example: `fun operate(a: Int, b: Int, op: (Int, Int) -> Int)`|
|Returns a function|Example: `fun getOperator(type: String): (Int, Int) -> Int`|
|Function reference (`::`)|Example: `operate(5, 3, ::add)`|
|Lambda expressions|Example: `{ x, y -> x + y }`|
|Inline functions|Optimized for performance, avoids object creation|