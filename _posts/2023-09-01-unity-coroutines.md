---
layout: post
title:  "Da Heck Are Coroutines?"
categories: unity
author: Jelani
---

There isn't a good parallel for courintes in web development (that I know of) so it's difficult for me to internalize.

## What Are They?

Normally when you execute code inside the `Update` function, it will run and complete within the current frame.

**Coroutines** allow you to evaluate game logic over _multiple_ frames.

With coroutines, you can pause a function and tell it to wait for a condition or action to occur before continuing.

This also means you can split up its functionality into a number of steps that can be executed in order.

## When Should You Use One?

When you:
- need to have a function wait for another action to finish.
  Like when you're:
  - moving an object to a position.
  - giving an object a list of tasks to carry out
- want to pause an action halfway.
  Like when you're:
  - queuing up a series of actions to take place one after another
  - fading visuals or audio in and out.
  - waiting for resources to load.

## Basic Usage

1. Define a function that returns an `IEnumerator`.

```c#
IEnumerator MyCoroutine() {
  // ...
}
```

2. Decide how/where you want to function to pause. You can think of `yield` as "pause until ___", if it helps.

  - `yield return null` tells Unity to **wait until the next frame before continuing**.
  - `yield return new WaitForSeconds(n)` tells Unity to **wait for a specific number of seconds before continuing**.
    - There's a similar `WaitForSecondsRealtime` function you can use.
  - `yield return StartCoroutine(MyOtherCoroutine())` tells Unity to **wait for `MyOtherCoroutine` to finish before continuing**.
  - `yield return new WaitForEndOfFrame()`tells Unity to **wait until the _next_ frame begins before continuing**.
  - `yield return new WaitUntil(x)` pauses execution until a <u>delegate</u> evaluates to `true`.
  - `yield return new WaitWhile(x)` pauses execution until a delegate evaluates to `false`.

I've only run into use cases for the second and third one so far, but I'll keep the rest for reference.

3. Run the coroutine with `StartCoroutine(MyCouroutine);`

### Reference

- [Couroutines in Unity - when and how to use them](https://gamedevbeginner.com/coroutines-in-unity-when-and-how-to-use-them/)
