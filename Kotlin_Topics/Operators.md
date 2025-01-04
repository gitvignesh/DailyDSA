### == and ===

| **`==` (Structural Equality)**                | **`===` (Referential Equality)**                   |
| --------------------------------------------- | -------------------------------------------------- |
| Compares contents (via `equals()`)            | Compares memory references (identity)              |
| Yes (`equals()` can be overridden)            | No (Cannot be overridden)                          |
| `Any.equals()` compares reference by default  | Always checks references directly                  |
| Checking if two objects have the same content | Checking if two variables point to the same object |
Notes:
1. For primitives both are same as compared by value
2. For String both are same as strings in interned in kotlin