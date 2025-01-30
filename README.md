# React useEffect Hook Missing Dependency

This repository demonstrates a common error in React's `useEffect` hook: missing dependencies in the dependency array.  This can lead to unexpected behavior and difficult-to-debug issues.

## The Problem

The `useEffect` hook in the `bug.js` file is missing `count` from its dependency array. This means that the effect runs after every render, regardless of whether the `count` value has changed.  This can cause the console to log the count repeatedly and unexpectedly.

## The Solution

The `bugSolution.js` file shows the corrected code.  By including `count` in the dependency array, the effect only runs when `count` changes, ensuring the correct behavior.

## How to Reproduce

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to run the application.
5. Observe the console output in `bug.js` and compare it to the output in `bugSolution.js`. 

## Lessons Learned

Always carefully consider which values the `useEffect` hook should depend on.  Missing or incorrect dependencies are a frequent source of errors in React applications.  The React documentation provides thorough guidelines on using the `useEffect` hook correctly.