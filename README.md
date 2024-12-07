# React UseEffect setInterval Memory Leak

This repository demonstrates a common error in React applications: memory leaks caused by improper use of the `setInterval` function within the `useEffect` hook.

The `bug.js` file contains the erroneous code.  The `setInterval` function is used to update a counter every second, but it lacks a cleanup function to clear the interval when the component unmounts. This leads to a memory leak.

The `bugSolution.js` file provides the corrected code, incorporating a cleanup function to clear the interval when the component is unmounted, thereby preventing the memory leak.  This ensures efficient memory management within the React application.

## How to Reproduce the Bug
1. Clone this repository.
2. Run `npm install`
3. Run the app (Instructions may vary depending on your setup)
4. Observe that the memory usage increases over time due to the memory leak.