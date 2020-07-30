---
layout: post
title: On the adoption of Kotlin as the language of choice for LEIC’s introductory course to programming
date: 2020-05-08
type: post
published: true
status: publish
categories: []
tags: []
author:
  login: palbp
  email: 
  display_name: Paulo Pereira
  
---

Starting next semester, Kotlin will be adopted as the introductory programming
language in LEIC’s curricular program, in the
[Programming](https://www.isel.pt/en/subjects/programming-leic) course.
Newcomers to
[ISEL’s LEIC](https://isel.pt/en/courses/bsc-degree/computer-science-and-engineering)
will start their programmer’s journey with Kotlin, rather than using Java. Why
did we move from Java to Kotlin? Why not some other language instead?

We have been using the Java language since 2005, given the importance of the
Java platform in the software industry. That importance is still indisputable.
The JVM is targeted by numerous programming languages [[1](https://en.wikipedia.org/wiki/Java_(software_platform)#Languages)][[2](https://en.wikipedia.org/wiki/List_of_JVM_languages)] and the Java
language is one of the most widely used [[3](https://www.jetbrains.com/lp/devecosystem-2019/)][[4](https://insights.stackoverflow.com/survey/2019?#technology)]. The Java ecosystem, i.e. tools
and frameworks, is vast and comprehensive: it is relevant both on the
server-side and on the client-side. [[1](https://en.wikipedia.org/wiki/Java_(software_platform)#Languages)]

Yet we should not mistake the platform for the language. The platform’s current
relevance is not determined by the language’s relevance, which has been
criticized almost since its inception. [[2](https://en.wikipedia.org/wiki/List_of_JVM_languages)][[3](https://www.jetbrains.com/lp/devecosystem-2019/)] Despite the criticisms, the
importance of the language is undeniable. [[3](https://www.jetbrains.com/lp/devecosystem-2019/)][[4](https://insights.stackoverflow.com/survey/2019?#technology)] But even more relevant than the
language itself, however, is Java’s ecosystem and particularly the JVM. The
number of languages that target it is a clear testimonial.

Regardless of the criticisms of the language design, the pervasive use of Java’s
ecosystem in the software industry implies that it must be addressed in LEIC’s
curriculum.

Additionally, the choice of the first programming language to be used in LEIC
curriculum should be guided by the following requirements:

* Usable in the Java ecosystem
* Multi-paradigm, similarly to the most widely used languages in the software industry
* With static typing, so that there is a formal contract verifier

These requirements have the following benefits: by being usable in the Java
ecosystem, it will make students familiar with that ecosystem; by being
multi-paradigm, it will not impose a programming style at such an early stage of
learning; by requiring a formal contract verifier, there’s an imposition of a
contract specification discipline that does not come naturally to apprentices.

So why not simply continue to use the Java language? In order to remain
multi-paradigm, the Java language has undergone several changes, but precisely
for that reason, it already shows the scars of time: some of its constructs
reveal design tradeoffs to guarantee backward compatibility, in particular the
constructs that were added to support the functional programming style whose
relevance in the mainstream of the software industry has been increasing. These
marks of time impair its pedagogical use. How can Java’s functional interfaces
and default methods be explained to a newcomer? With difficulty. 

Java’s functional interfaces are not in fact the biggest pedagogical challenge
in using Java as an introductory language to programming. See, for example, the
customary “Hello World” program, written in Java:

<pre><code class="language-java">
public class App {
   public static void main(String[] args) {
      System.out.println("Hello World!");
   }
}
</code></pre>

It requires a great deal of goodwill to be able to see the message that should
be conveyed to the students when the program is presented. Let’s now look at the
same program, written in Kotlin [[5](https://kotlinlang.org/)]:

<pre><code class="language-java">
fun main() {
   println("Hello World")
}
</code></pre>

The difference is obvious. The problem is that the Java language was designed
with the assumption that functions must always be defined in the context of a
type definition, be it a class or an interface (the sacrifice of verbs to nouns,
so brilliantly described here [[6](http://steve-yegge.blogspot.com/2006/03/execution-in-kingdom-of-nouns.html)]. This cannot be explained to an apprentice
unless it’s seen from a 90’s perspective, which is not useful at this early
stage of learning.

Considering the increasing credibility and popularity [[3](https://www.jetbrains.com/lp/devecosystem-2019/)][[4](https://insights.stackoverflow.com/survey/2019?#technology)] of the Kotlin
programming language, and because it fully meets our requirements, its selection
became natural. We also have been using it in several LEIC courses, namely: in
[Mobile Devices Programming](https://www.isel.pt/en/subjects/mobile-devices-programming-leic) since 2016 and in [Web Application Development](https://www.isel.pt/en/subjects/web-application-development-leic) since
2018.

And there you go: next semester, newcomers to our beloved craft will be greeted
with an introduction to programming using Kotlin. Time will judge our audacity.