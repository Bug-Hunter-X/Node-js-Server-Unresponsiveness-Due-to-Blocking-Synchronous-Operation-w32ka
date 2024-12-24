# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js applications: unresponsiveness due to blocking synchronous operations.  The server hangs when a long-running task is performed synchronously, preventing it from responding to further requests.

## Problem

The `server.js` file contains a Node.js HTTP server that performs a computationally intensive task synchronously within the request handler. This blocks the event loop, making the server unresponsive to new requests.

## Solution

The `serverSolution.js` file demonstrates the solution: offloading the long-running task to a worker thread or using asynchronous operations to prevent blocking the event loop.