---
layout: academia/leic/lae
goals: |
  A student completing this course unit should be able to:
  1. Compare and use different common constructs in modern programming
     languages, mapping different programming paradigms, and their support in
     the execution environment.
  2. Understand the main constituents of managed runtimes, and know how to
     compare different type systems approaches in these environments.
  3. Use runtime metadata (reflection) to examine types and use metaprogramming
     to analyze and transform programs at runtime.
  4. Analyze the performance of managed programs and efficiently use automatic
     memory management support (garbage collection).
syllabus: |
  <ol type="I">
    <li>
      Main constructions of languages supported in managed runtimes, and their
      contextualization in different programming paradigms, using as main case study
      the Java Virtual Machine (JVM).
    </li>
    <li>
      Main constituents of managed runtimes, namely: class loader, verifier,
      just-in-time compiler, metadata and memory management.
    </li>
    <li>
      Comparison of type systems for managed runtimes regarding: equivalence rules,
      compatibility and inference.
    </li>
    <li>
      Java reflection API and metaprogramming case studies in software development.
    </li>
    <li>
      Execution stack model and records. Analysis of the main Java bytecode
      instructions supported by tools for structural reflection (e.g. ASM, Javassist).
     </li>
    <li>
      Introduction to the performance analysis of programs written in Java, and the
       use of monitoring tools for the JVM (e.g. jconsole).
    </li>
    <li>
      Introduction to garbage collection algorithms in the JVM.
    </li>
  <ol>
outcomes: |
  This course identifies the main problems solved by runtimes for high-level
  languages and the support they provide for application development. In
  particular, it analyzes constructions available in high-level languages and
  their type systems, using Java as the main case study.
  
  The consistency between the syllabus and the objectives of the course is as follows:
  
  - Objective 1 is achieved through contents I and III;
  - Objective 2 is achieved through contents II, III, and IV;
  - The contents IV and V contribute to objective 3;
  - The contents V, VI and VII aim to achieve objective 4.
---
