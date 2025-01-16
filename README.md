# Node.js Server Unresponsiveness Due to Synchronous Long-Running Task

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in the request handler blocks the event loop, causing the server to become unresponsive.  The `server.js` file contains the buggy code, while `serverSolution.js` provides a corrected version using asynchronous operations.

**Problem:**
The original code uses a `while` loop to simulate a 5-second delay.  This synchronous operation blocks the event loop, preventing Node.js from processing other requests and potentially leading to a timeout or hang.

**Solution:**
The solution involves using asynchronous techniques, such as `setTimeout` or promises, to avoid blocking the event loop.  The improved code ensures that the server remains responsive even during long-running operations.