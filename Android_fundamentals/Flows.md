Flows are Kotlin language feature that serves as a reactive programming framework. it's all about being notified about the changes in the code and sending it through a pipeline and potentially modifying it. A flow at core is a coroutine that can emit multiple values over a period of time. Flow is like a stream of data constituted of three components:
1. **_Producer:_** produces data that is added to the stream. Thanks to coroutines, flows can also produce data asynchronously
2. **_Intermediary:_** Optional component that can modify each value emitted into the stream or the stream itself
3. **_Consumer:_** consumes the value from the stream

### Flow Producers and Types
1. flow { } : this is cold stream and is triggered only on collection 
2. stateFlow : hold of value as hot stream
3. sharedFlow : one time events as hot stream

### Flow Operators
1. filter { }: will give only the valid fields that pass the check
2. map { }: will convert the field to result based on some operation
3. onEach { }: operate on each flow emitted value
		 **Emission Forwarding Operators**
4. buffer (): Let the producer run and not wait for the consumer sequence is maintained 
5. conflate (): like collectLatest drop intermediate emissions while buffering. 
         **Terminal Operators**
6. count { }: give number of emits that match a condition
7. reduce { accumulator, value }: it accumulates all the emits and give the end result
8. fold (initial) {accumulator, value }: same as reduce but we can provide a initial value 
9. flatMapConcat { }
10. flatMapMerge { }
11. flatMapLatest { }

### Flow Consumers
1. collect
2. collectLatest


