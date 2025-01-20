# React useEffect Hook Memory Leak
This example demonstrates a common error in React applications using the useEffect hook: memory leaks due to missing cleanup functions. 

The `setInterval` function inside the `useEffect` hook continues to run even after the component unmounts, causing a memory leak. The solution demonstrates how to correctly use the cleanup function to prevent this. 

## How to Reproduce
1. Clone the repository
2. Run `npm install`
3. Run `npm start`
4. Observe the counter incrementing.  Unmounting the component will not stop the counter, indicating a memory leak.

## Solution
The solution implements a cleanup function that clears the interval when the component unmounts, preventing memory leaks.