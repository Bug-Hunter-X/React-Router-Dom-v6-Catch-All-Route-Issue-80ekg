# React Router Dom v6 Catch All Route Issue

This repository demonstrates a common issue encountered when using the catch-all route (`/*`) in React Router v6. The problem is that the catch-all route is always triggered, even when navigating to valid routes. This is unexpected behavior because the catch-all route should only be triggered when no other routes match.

## Bug

The bug is present in `App.js`. The catch-all route (`/*`) is placed after other routes, causing the issue.  Even when navigating to `/` or `/about`, the NotFound component is displayed.

## Solution

The solution (`AppSolution.js`) moves the catch-all route to the end of the route definitions to fix the issue. This ensures that other routes are checked first before the catch-all is considered.