---
layout: academia/leic/pc
lang: en
goals: |
  Students who successfully complete this course unit will be able to:
  1. Correctly develop application-level programs for execution in multi-threaded environments, with emphasis on managed platforms such as the JVM (Java Virtual Machine) and the .NET platform. Identify and correctly handle concurrency scenarios, including the design of custom synchronizers and the guarantees provided by memory models.
  2. Correctly use the common application-level asynchronous programming models available, namely futures, asynchronous methods, coroutines, and reactive streams.
syllabus: |
  1. Fundamental concepts: threads and execution context switching, data sharing concurrency and associated hazards.
  2. Characterization of the threading model for typical application types, namely UI-based applications and HTTP servers.
  3. Identification of data sharing concurrency hazards and techniques for their elimination, including immutability, thread affinity, mutual-exclusion, and proper object publication. 
  4. Coordination between threads, the synchronizer concept and their implementation using monitors.
  5. The concept of memory model and its use to correctly implement concurrency scenarios.
  6. Thread management techniques and thread pools.
  7. The concept of asynchronous I/O and the motivation for asynchronous programming models. Models and mechanisms for asynchronous programming: futures, asynchronous methods, coroutines and reactive streams. Asynchronous coordination between threads.
outcomes: |
  Items (1) to (5) of the syllabus provides the knowledge required to correctly develop programs on multithreaded contexts, including proper data synchronization and thread coordination, therefore addressing the first learning outcome.
  Items (6) and (7) of the syllabus provides the additional knowledge for the development of asynchronous programs, addressing learning outcome (2), including the interaction between asynchronous models and multithreading.
---
