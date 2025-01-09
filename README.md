# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving an infinite loop caused by the `useEffect` hook. The `useEffect` hook, when used without specifying dependencies, runs after every render, leading to an uncontrolled state update cycle.  This can significantly impact performance and application stability.

## How to Reproduce

Clone this repository and run the application. You'll observe that the console continuously logs the count, and the application becomes unresponsive due to the infinite loop. 

## Solution

The solution involves correctly specifying the dependencies array in the `useEffect` hook.  By providing the `count` variable as a dependency, `useEffect` only runs when `count` changes, preventing the infinite loop.