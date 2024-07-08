To Understand what is coroutine and its need first we have to grasp what is [[Process & Thread]].

Coroutines is a framework that work on threads under the hood. There are 2 important components for a coroutine 
1. Scope: It defines the lifetime of the coroutine
2. Context: It defines the threads that can be used
### Scopes
1. GlobalScope
2. lifecycleScope
3. vewModelScope
### Dispatcher
Define set of threads (Thread Pool) that can be used for the coroutine
1. Dispatchers. Main : Confined
2. Dispatchers. Unconfined
3. Dispatchers. IO
4. Dispatchers. Default
### Methods to start a coroutine
1. launch 
2. async
3. runBlocking
4. withTimeout(timeMillis)
5. withContext(Dispactcher)
### Other Methods
1. cancel: End the coroutine 
2. join: Wait for the completion
3. isActive: Is current coroutine active
4. await: Wait till the deferred object of async is returned 

