###  Next.js App



To build a complete web application with React from scratch, there are many important details you need to consider:

Code has to be bundled using a bundler like webpack and transformed using a compiler like Babel.
You need to do production optimizations such as code splitting.
You might want to statically pre-render some pages for performance and SEO. You might also want to use server-side rendering or client-side rendering.
You might have to write some server-side code to connect your React app to your data store.
A framework can solve these problems. But such a framework must have the right level of abstraction — otherwise it won’t be very useful. It also needs to have great "Developer Experience", ensuring you and your team have an amazing experience while writing code.

Next.js: The React Framework
Enter Next.js, the React Framework. Next.js provides a solution to all of the above problems. But more importantly, it puts you and your team in the pit of success when building React applications.

Next.js has the best-in-class "Developer Experience" and many built-in features; a sample of them are:

An intuitive page-based routing system (with support for dynamic routes)
Pre-rendering, both static generation (SSG) and server-side rendering (SSR) are supported on a per-page basis
Automatic code splitting for faster page loads
Client-side routing with optimized prefetching
Built-in CSS and Sass support, and support for any CSS-in-JS library
Development environment with Fast Refresh support
API routes to build API endpoints with Serverless Functions
Fully extendable


**Basic CSS example
Next.js has built-in support for CSS Modules allowing you to write scoped CSS by automatically creating a unique class name. CSS Module files can be imported anywhere in your application and you don't have to worry about collisions.**

Deploy your own
Deploy the example using Vercel:

Deploy with Vercel

How to use
Execute create-next-app with npm or Yarn to bootstrap the example:
```javascript
npx create-next-app --example basic-css basic-css-app
# or
yarn create next-app --example basic-css basic-css-app
```
