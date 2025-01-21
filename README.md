# Unresponsive Node.js Server
This repository demonstrates a common issue in Node.js: an unresponsive server caused by a long-running synchronous operation that blocks the event loop.  The `blockingServer.js` file showcases the problem, while `nonblockingServer.js` provides a solution using asynchronous operations.

## Problem
Node.js is single-threaded, meaning that only one operation can be processed at a time.  Long-running synchronous operations in the request handler directly block the event loop, preventing the server from responding to other requests.  This results in an unresponsive server and potential performance issues.

## Solution
The solution is to use asynchronous operations to avoid blocking the event loop.  This allows the server to continue processing requests while the long-running task is being performed.

## How to Run
1. Clone this repository
2. Navigate to the directory
3. Run `node blockingServer.js` to see the unresponsive server
4. Run `node nonblockingServer.js` to see the corrected solution
