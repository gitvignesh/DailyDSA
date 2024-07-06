Lets understand what is a process briefly. Process is the fundamental structure that is required to run any code. In a process, Thread is the atomic unit that is scheduled for execution, we can say process is like a container for resources and execution. Without a Process there can be no thread.

==**Minimum requitements for a process:==**
1. Text segment : code
2. Program counter: Next instruction address
3. Stack: Local Variables, function parameters
4. Heap: Dynamically allocated memory.
5. Data Segment: Global and static variables.
6. Process State: Current status (new, ready, running, waiting, terminated).
7. PCB: Contains process-specific information (ID, state, CPU registers, memory management, scheduling, accounting, I/O status).

**==Minimum requirements for a thread:==**
1. Thread ID (TID): Unique identifier for distinguishing threads within a process, managed by the operating system.
2. Program Counter (PC): Next instruction address
3. Stack: Dedicated memory area for storing local variables, function parameters, and execution context, ensuring thread-specific data integrity.
4. Thread State: Represents the current status of the thread (running, ready, waiting, terminated), managed for scheduling and execution control.
5. CPU Registers: Includes registers such as program counter and stack pointer, crucial for efficient thread execution and context switching.