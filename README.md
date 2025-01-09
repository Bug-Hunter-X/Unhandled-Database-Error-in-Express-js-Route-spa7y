# Unhandled Database Error in Express.js Route

This repository demonstrates a common error in Express.js applications:  lack of error handling for database queries within route handlers.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides a corrected version.

## Problem

The `bug.js` file shows an Express.js route that fetches user data from a database.  It correctly handles the case where a user is not found. However, it lacks error handling for database errors (e.g., connection errors, query errors).  If a database error occurs, the server might crash or respond with an unexpected error.

## Solution

The `bugSolution.js` file demonstrates the corrected code.  It uses a `try...catch` block to wrap the database query.  If an error occurs during the query, a proper error response (e.g., 500 Internal Server Error) is sent to the client, preventing the server from crashing and providing informative feedback.