# React Router v6 Catch-all Route Conflict

This repository demonstrates a common issue in React Router v6 where the catch-all route (`/*`) conflicts with other defined routes. The issue arises when the catch-all route is placed before more specific routes, causing it to match all paths and preventing the other routes from being accessed.

## Problem

The provided `App.js` demonstrates the issue where the `/*` route prevents the `/about` route from functioning correctly.  Navigating to `/about` will always redirect to the `NotFound` component.

## Solution

The `AppSolution.js` file demonstrates the solution to this problem. The catch-all route is moved to the end of the route definitions in the `Routes` component to ensure it only matches routes that do not match any other previously defined routes.