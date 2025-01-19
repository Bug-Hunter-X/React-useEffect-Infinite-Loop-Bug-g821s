# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook and missing dependencies.  The `useEffect` hook is designed to perform side effects after every render, but if its dependencies are not correctly specified, it can lead to infinite render loops and performance issues. This example showcases the error and its solution.

## Bug Description

The initial code has an `useEffect` hook that logs the current value of the `count` state variable.  However, the `count` variable is missing from the dependency array. This means the effect will run after every render, regardless of changes to `count`, continuously updating the console and creating an infinite render loop. 

## Solution

The solution involves adding `count` to the dependency array, ensuring the effect runs only when the value of `count` changes.