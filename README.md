# Node.js Server Hang - Long-Running Synchronous Operation

This repository demonstrates a common Node.js issue: a server becoming unresponsive due to a long-running synchronous operation blocking the event loop. The `bug.js` file shows the problematic code, while `bugSolution.js` provides a corrected version using asynchronous programming.

## Problem

The `bug.js` file contains a simple HTTP server. However, it includes a `while` loop that simulates a long-running task. This loop blocks the event loop, preventing the server from handling other requests and potentially leading to hangs or unresponsiveness.

## Solution

The `bugSolution.js` file addresses this by replacing the synchronous `while` loop with asynchronous operations.  This allows the event loop to continue processing other events while the long-running task completes in the background.