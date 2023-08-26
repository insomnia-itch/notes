---
layout: post
title:  "Arrays in Unity"
categories: unity
author: Jelani
---


I'm so Ruby-pilled that I forget how Arrays were made back in the day 🧓

## Declaration

It works like:

```
<Class Type>[] variableName;
```

For example:
```c#
int[] integers;
GameObject[] objects;
```

## Instantiation

```c# 
// Creates size with empty elements
int[] numbers = new int[5];
```

## Instantiate with specific elements

This is the weirdest part— since you use curly braces instead of brackets.

```c#
int[] numbers = { 1, 2, 3, 4 };
```

### Selecting Random Object

This is useful when you want to randomly spawn an object from a list of prefabs.

```c#
GameObject[] obstacles = { lowObstacle, mediumObstacle, highObstacle };
index = UnityEngine.Random.Range(0, obstacles.length);
spawnObstacle = obstacles[index];
spawnPosition = new Vector3(...);
Instantiate(spawnObstacle, spawnPosition, Quaternion.identity);
```
