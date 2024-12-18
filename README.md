# React Memory Leak with setInterval in useEffect

This repository demonstrates a common error in React applications: memory leaks caused by improper use of the `setInterval` function within the `useEffect` hook.

The `bug.js` file contains the problematic code.  `setInterval` is used without a cleanup function, leading to a memory leak as the interval continues to run even after the component unmounts.

The `bugSolution.js` file provides the corrected code, including a cleanup function that uses `clearInterval` to stop the interval when the component is unmounted. This prevents the memory leak.

## How to Reproduce

1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server. 
4. Observe the behavior (count increasing continually in the console).
5. Refer to bugSolution.js to see how to resolve this issue.