
### Classes in kotlin

| **`class`**                                          | **`open class`**                      | **`sealed class`**                                                 | **`abstract class`**                     | **`enum class`**                                         |
| ---------------------------------------------------- | ------------------------------------- | ------------------------------------------------------------------ | ---------------------------------------- | -------------------------------------------------------- |
| Default class for creating objects, Fina by default. | Allows inheritance                    | Restricts inheritance to known subclasses within the same package. | Base class with incomplete functionality | Represents a fixed set of constants, cannot be inherited |
| Can be instantiated                                  | Can be instantiated                   | Cannot be instantiated directly                                    | Cannot be instantiated directly          | Cannot be instantiated directly                          |
| Not allowed                                          | Not allowed                           | Not allowed                                                        | Allowed                                  | Not applicable                                           |
| Type safety depends on implementation                | Type safety depends on implementation | Compiler ensures exhaustive handling                               | Type safety Depends on implementation    | Exhaustive switch handling                               |
