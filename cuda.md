### GPU programming specialization

- Parallel programming in my repository: [Parallel Programming](https://github.com/iliasslasri/concurrent-programming)
- [CUDA Programming](https://www.coursera.org/specializations/gpu-programming)

#### Concurrent programming
- Pitfalls in concurrent programming:
    - Ressource Contention: When two threads try to access the same resource at the same time.
    - Deadlocks similar to resource contention, but with multiple resources. A deadlock occurs when two or more threads are waiting for each other to release a resource, which they have locked.
    - Race Conditions: When two threads try to access the same memory location at the same time, and at least one of them is writing to it. This can lead to unpredictable behavior. We should minimize shared memory addresses between threads.
    - Live lock is a variant of dead lock in which at least one of the threads in lock, will actively do something but still cannot leave the locked state.
- Semaphores are for all intents and purposes is an atomic variable that have more than one thread acquire it, which means that a predefined number of threads can use the semaphore to enter a critical section of code. A lock is the more restrictive parent asynchronous mechanism for a single thread to enter a critical section of code. Thus a semaphore is a more relaxed form of lock.

- Canonical challenges :
  - _Dining Philosphers_ : A classic problem in concurrent programming. The problem consists of five philosophers sitting at a table doing one of two things: eating or thinking. While eating, they are not thinking, and while thinking, they are not eating. The philosophers sit at a circular table with a large bowl of spaghetti in the center. There are five forks for them to share. To eat, a philosopher must have forks in both their left and right hands. The problem is how to design a discipline of behavior (a concurrent algorithm) such that each philosopher won't starve; i.e., can eat infinitely often. [Solution to Dinning Philosophers](https://www.adit.io/posts/2013-05-11-The-Dining-Philosophers-Problem-With-Ron-Swanson.html)
  - _Producer Consumer_, reader writer.
  - _Sleeping Barber_ : The problem consists of a barber shop with a barber, a waiting room with a number of chairs, and a number of customers. The barber is asleep until a customer arrives. When a customer arrives, the barber wakes up and cuts the customer's hair. If there are no customers, the barber goes back to sleep. The problem is how to design a discipline of behavior (a concurrent algorithm) such that the barber and the customers can do their work without colliding with each other.
  - _Data and code synchronization_ : The problem consists of a data structure that is shared among multiple threads. The data structure is a list of integers. The threads can read and write to the list. The problem is how to design a discipline of behavior (a concurrent algorithm) such that the threads can read and write to the list without colliding with each other.

- Concurrent Programming Patterns:
  - Divide and conquer: A parallel algorithm design paradigm that solves a problem by dividing it into smaller subproblems, solving the subproblems in parallel, and combining the solutions to the subproblems to solve the original problem. The parallelism comes from the fact that the subproblems can be solved in parallel. The divide-and-conquer paradigm is used in many parallel algorithms, such as quicksort, mergesort, and matrix multiplication.
  - MapReduce: A parallel algorithm design paradigm that solves a problem by dividing it into smaller subproblems, solving the subproblems in parallel, and combining the solutions to the subproblems to solve the original problem. The parallelism comes from the fact that the subproblems can be solved in parallel. The MapReduce paradigm is used in many parallel algorithms, such as word count, matrix multiplication, and graph algorithms.
  - Repository : manages central state across multiple running processes. Processes access amd update their own and central state through predefined communications mechanisms. Need to ensure that two processes don't update the same state at the same time.
  - Pipelines and workflows are similar patterns that involve the flow of data from one step to another. Pipelines have a linear flow, while workflows can have cycles. These patterns are useful for dividing tasks into smaller steps and coordinating the flow of data. Pipelines are the simplest form of directed acyclic graphs (DAGs). They definitely have no cycles and they proceed from one step to another without any more advanced branching schemes such as forks and joins
  - Recursion is a powerful technique where a function calls itself to solve a problem. It can be used to solve complex problems by dividing them into smaller subproblems. However, recursion requires careful management of state and may not be suitable for large datasets or distributed systems.

- Flynn's Taxonomy: SISD, SIMD, MISD, MIMD, see my other projects for more details.

- Python3 :
  - _thread/ threading libraries
  - asyncio library
  - multiprocessing library : The multiprocessing library is very powerful as it takes the idea of independent execution of threads inside of a Python 3 context and allows for execution of code outside of the current calling process and even on a remote machine. Spawn, fork and forkserver, all have three general goals. Create new processes out of the current process, though they have different results.

#### CUDA Programming

#### Parallel Programming Resources :

Cornell University - Functional Programming with OCaml Open Source Textbook - [textbook](https://cs3110.github.io/textbook/cover.html)

MachineLearningPlus Parallel Programming in Python - [tutorial](https://www.machinelearningplus.com/python/parallel-processing-python/)


-> Stopped at First lecture of Module 4 : Integrated versus Dedicated GPUs