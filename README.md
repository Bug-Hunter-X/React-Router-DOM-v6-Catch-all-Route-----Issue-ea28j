# React Router DOM v6 Catch-all Route '*' Issue

This repository demonstrates a common issue encountered when using the catch-all route ('*') in React Router DOM v6. The problem is that the catch-all route doesn't render when navigating to a non-existent path, even though it should be the default fallback.

## Problem Description
The provided code uses React Router's `Routes` and `Route` components to define routes. While the routes for '/' and '/about' work correctly, the catch-all route path='*' fails to render when a non-existent path is accessed.  This behavior differs from expectations of a catch-all route.

## Solution
The solution involves correctly placing the catch-all route at the end of the `Routes` component. By moving the `Route path="*"` below other defined routes, the router will check all other routes first before rendering the catch-all route for undefined paths.
