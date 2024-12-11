# Unhandled Errors in Node.js HTTP Server

This repository demonstrates a common error in Node.js: failing to handle potential errors in an HTTP server.  The `bug.js` file shows a basic server that lacks error handling.  The `bugSolution.js` file provides a corrected version that gracefully handles errors.

## Bug Description

The original code creates an HTTP server but doesn't include any error handling. If the port is already in use or another error occurs during server creation or operation, the server will crash without providing any informative error messages.

## Solution

The corrected version uses the `error` event listener to capture and handle errors, preventing unexpected crashes.  It logs the error to the console for debugging and exits gracefully.