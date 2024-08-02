Implement a circular buffer in kotlin

Solution:
```kotlin
import kotlin.collections.ArrayDeque

// TODO: implement proper exceptions to complete the task
class EmptyBufferException: Exception("Buffer is empty")

class BufferFullException: Exception("Buffer is full")

class CircularBuffer<T>(private val size:Int = 10) {
    private val store = ArrayDeque<T>(size)

    fun read() : T {
        if (store.isEmpty()) {
            throw EmptyBufferException()
        } else {
            return store.removeFirst()
        }
    }

    fun write(value: T) {
        if (store.size == size) {
            throw BufferFullException()
        } else {
            store.addLast(value)
        }
    }

    fun overwrite(value: T) {
        if (store.size != size) {
            write(value)
        } else {
            read()
            write(value)
        }
    }

    fun clear() {
        store.clear()
    }
}
```

Topics: [[Collections]]