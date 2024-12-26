# Kotlin removeIf gotcha!

This repository demonstrates a subtle bug in Kotlin related to using the `removeIf` function with Maps.  The `keys` property of a `MutableMap` is not directly mutable, so attempting to modify it with `removeIf` results in unexpected behaviour.  The included example shows this behaviour and also provides a solution.

## Bug

The file `bug.kt` contains code that illustrates this issue. `removeIf` will not remove the element from the map if applied to a `keys` set, leading to incorrect results.

## Solution

The file `bugSolution.kt` provides a corrected version of the code, demonstrating the proper way to remove elements from a `MutableMap`.