# Infinite useEffect Loop Bug in React

This repository demonstrates a common React bug: an infinite loop caused by a missing dependency in the `useEffect` hook.  The `useEffect` hook is intended to perform side effects, but without proper dependency management, it can lead to unexpected behavior and performance issues.

## Bug Description

The provided `MyComponent` uses `useEffect` to log the current count to the console.  However, because `count` is not included in the dependency array, the effect runs on every render, causing an infinite loop of logging.

## Solution

The solution involves adding `count` to the dependency array.  This ensures that the effect only runs when `count` changes, fixing the infinite loop.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`. Observe the continuous logging in the console.
4. Examine the `bugSolution.js` file for the corrected code.