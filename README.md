# React useEffect Dependency Array Issue

This repository demonstrates a common error in React's `useEffect` hook: omitting state variables from the dependency array.  Incorrectly managing the dependency array can lead to unexpected re-renders and potential bugs.

## The Problem

The `bug.js` file contains a component with a `useEffect` hook. This hook logs the current `count` value on every render.  However, because `count` is *not* included in the dependency array, the effect runs on every render regardless of changes in `count`, resulting in unnecessary console logging.

## The Solution

The `bugSolution.js` file corrects this by adding `count` to the dependency array. Now, the effect only runs when `count` changes, improving performance and preventing unexpected behavior.

## How to run

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install the dependencies.
4. Run `npm start` to start the development server. 

This will display a simple counter component.  Examine the console logs to see the difference between the correct and incorrect implementations.