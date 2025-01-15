# React Router v6 Catch-all Route Issue

This repository demonstrates an uncommon issue with React Router v6's catch-all route (`/*`).  The catch-all route unexpectedly intercepts all requests, preventing other, more specific routes from matching.  The solution involves careful route ordering and potentially leveraging `useLocation` hook for more complex scenarios.

## Problem

The `/*` route in `App.js` is intended to handle 404 errors. However, it intercepts all requests, even those that should match other defined routes, such as `/about`.

## Solution

The `AppSolution.js` file provides a corrected version. The solution moves the catch-all route to be the last route defined in the `Routes` component, ensuring it's only used when no other route matches.