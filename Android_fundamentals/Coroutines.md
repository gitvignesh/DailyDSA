To Understand what is coroutine and its need first we have to grasp what is [[Process & Thread]].

Coroutines is a framework that work on threads under the hood. There are 2 important components for a coroutine 
1. Scope: It defines the lifetime of the coroutine
2. Context: It defines the threads that can be used

### Dispatcher
Define set of threads (Thread Pool) that can be used for the coroutine
1. Dispatchers. IO
2. Dispatchers. Main
3. Dispatchers. Default
### Methods to start a coroutine
1. launch 
2. async
3. runBlocking

