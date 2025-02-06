# React useEffect setInterval Memory Leak
This example demonstrates a common error in React: using `setInterval` within `useEffect` without proper cleanup. This leads to memory leaks and unexpected behavior.

The `bug.js` file contains the erroneous code. The `bugSolution.js` file provides the corrected version.

**Problem:**
The `setInterval` function, when used within `useEffect` without a cleanup function, continues to run even after the component unmounts. This results in memory leaks and might lead to unexpected behavior in other parts of the application.

**Solution:**
The solution involves returning a cleanup function from `useEffect`. This cleanup function will clear the `setInterval` when the component unmounts, preventing the memory leak.