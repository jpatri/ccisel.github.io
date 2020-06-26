---
layout: post
title: Java versus C# asynchronous abstractions
date: 2020-06-26
type: post
published: true
status: publish
categories: []
tags: [Java, async, CompletableFuture, Task]
author:
  login: miguelgamboa
  email: 
  display_name: Miguel Gamboa
  
---

Do you know the difference between the behavior of the two code snippets that
answer the question
[“Java Equivalent of C# async/await?”](https://stackoverflow.com/q/16539245/1140754)?

With almost 100K views on Stackoverflow, many developers are still looking for
alternatives to Java absence of the well-known `async`/`await` idiom found in most
programming languages such as Js, C#, Kotlin or Python. 
Almost two years after the original post, the CCISEL engineer Miguel Gamboa has
presented a Java non-blocking alternative to get the body size of an HTTP
request response, which is still attracting increasing attention.
Nevertheless, although concise and non-blocking this solution still presents a
subtle different behavior from C# async/await use case of the original post.
**Can you guess what is it?**

```csharp
async Task<int> AccessTheWebAsync()
{ 
   HttpClient client = new HttpClient();
   var urlContents = await client.GetStringAsync("http://msdn.microsoft.com");
   return urlContents.Length;
}
```

```java
CompletableFuture<Integer> AccessTheWebAsync()
{
   return asyncHttpClient()
      .prepareGet("http://msdn.microsoft.com")
      .execute()
      .toCompletableFuture()
      .thenApply(Response::getResponseBody)
      .thenApply(String::length);
}
```