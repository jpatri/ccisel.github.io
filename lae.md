---
layout: course
title:
  en: Languages and Managed Runtimes
  pt: Linguagens e Ambientes de Execução
repository: https://github.com/isel-leic-ave/
isel: https://isel.pt/disciplinas/linguagens-e-ambientes-de-execucao-leic-pn
year: 2nd
semester: 2nd
ects: 6
professor:
  display_name: Miguel Gamboa de Carvalho
goals: |
  A student completing this course unit should be able to:
  - Compare and use different common constructs in modern programming languages, mapping different programming paradigms, and their support in the execution environment.
  - Understand the main constituents of managed runtimes, and know how to compare different type systems approaches in these environments.
  - Use runtime metadata (reflection) to examine types and use metaprogramming to analyze and transform programs at runtime.
  - Analyze the performance of managed programs and efficiently use automatic memory management support (garbage collection).
syllabus: |
  <ol>
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
  </ol>
outcomes: |
  <p>
    This course identifies the main problems solved by runtimes for high-level
    languages and the support they provide for application development. In
    particular, it analyzes constructions available in high-level languages and
    their type systems, using Java as the main case study.
  </p>
  <p>
    The consistency between the syllabus and the objectives of the course is as follows:
    <ul>
      <li>Objective 1 is achieved through contents I and III;</li>
      <li>Objective 2 is achieved through contents II, III, and IV;</li>
      <li>The contents IV and V contribute to objective 3;</li>
      <li>The contents V, VI and VII aim to achieve objective 4.</li>
    </ul>
  <p>
bibliography: |
  <p>
    <em>"Optimizing Java: Practical Techniques for Improving JVM Application
    Performance"</em> by Chris Newland, James Gough, Benjamin J Evans. Released
    April 2018. Publisher(s): O'Reilly Media, Inc. ISBN: 9781492039259.
  </p>
  <p>
    <em>"Programming Language Pragmatics"</em> by Michael L. Scott, 2015. Publisher(s):
    Morgan Kaufmann Publishers.
  </p>
  <p>
    <em>"The Java Virtual Machine Specification"</em> Java SE 12 Edition” by Tim
    Lindholm, Frank Yellin, Gilad Bracha, and Alex Buckley. Released February
    2019. Publisher(s): Oracle America, Inc.
  </p>
---
