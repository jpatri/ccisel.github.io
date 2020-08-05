---
layout: post
title: Stretching Async/Await With Lambdas
image: 2020-07-10-miguel-async-await.png
date: 2020-07-09
type: post
published: true
status: publish
category: Concurrent Programming
tags: [Java, async, CompletableFuture, Task, Promise, Kotlin]
author:
  login: miguelgamboa
  email: 
  display_name: Miguel Gamboa
  image: miguel.jpg
  role: Software Developer
  
---

1. Can you figure out the difference resulting from the execution of the
   following code snippets? TIP: one performs requests concurrently and the
   other sequentially. Which one and why?

2. Is there any difference if you replace the _arrays_ pipeline (i.e.
   `map().reduce()`) that performs _eagerly_ with an _iterable_ pipeline (such as
   C# Linq) performing _lazily_? Is it still sequential or still concurrent? Why?

If you are a Java, Kotlin, C# or JavaScript developer you may find more use
cases and foundations in the article of CCISEL engineer Miguel Gamboa about
"[_Stretching Async/Await With Lambdas_](https://dzone.com/articles/lambdas-in-concurrency-with-non-blocking-io)"

<table>
<tr>
<td>

<pre><code class="language-javascript">
async function fetchAndSumBodiesLengthsλ(urls) {
  return urls
    .map(async (url, i) => {
      const resp = await fetch(url)  // 1. Fetch url
      const body = await resp.text() // 2. Read body
      return body.length             // 3. Get length
    })
    .reduce(async (l1, l2) => {
      return await l1 + await l2     // 4. Sum lengths
    })
}
</code></pre>

</td>
<td>

<pre><code class="language-javascript">
async function fetchAndSumBodiesLengths(urls) {
  let sum = 0
  for (const url of urls) {
    const res = await fetch(url)  // 1. Fetch url
    const body = await res.text() // 2. Read body
    const length = body.length    // 3. Get length
    sum += length                 // 4. Sum lengths
  }
  return sum
}
</code></pre>

</td>
</tr>
</table>