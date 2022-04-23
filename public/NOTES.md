# Next.js

## What is Next.js?

Next is a React frontend development web framework created by Vercel (Formerly Zeit) that enables functinality such as server-side rendering and static site generation

### Note:

Basic knowledge of JavaScript and React
Some stuff you need to know before learning nextjs are javascript and basic of React including the following:
- Creating components
- Using JSX
- Passing props
- Using state




### Server-side Rendering

Unlike a traditional React app where the entire application is loaded and rendered on the client
Next.js allows the first page load to be rendered by the server, which is great for SEO and performance

### Next.js Benefits

- Performance
- SEO
- Easy Page Routing
- API Routes
- Out of the box Typescript and Sass
- Static Site Generation
- Easy Deployment
- The Next.js development server has Fast Refresh enabled. When you make changes to files, Next.js automatically applies the changes in the browser almost instantly. No refresh needed! This will help you iterate on your app quickly.


### Development Environment

To create Next.js app, you will need two things
- Node.js,  (I am using version 16.13) to check version of your node, write in your cmd 
```command line
  node -v
```

- NPM: to check version of your node, write in your cmd 
 ```command line
  npm -v
```
- Code editor (I am using VS Code)



### Some of Next.js Commands

To starts the development server, run the following command
```
npm run dev
```

To build the app for production, run the following command
```
npm run build
```
if you want stop the server, just hit `Ctrl + c`

To runs the built app in production mode, run the following command
```
npm start
```

To export the app for static websites, run the following command
```
npm build & npm export
```

### Pages in Next.js

- In Next.js, a page is a React Component exported from a file in the pages directory.
- Pages are associated with a route based on their file name. For example, in development:
  - `pages/index.js` is associated with the `/` route.
  - `pages/posts/first-post.js` is associated with the `/posts/first-post route`
  
  
#### To can create different pages in Next.js.

Simply create a JS file under the 'pages directory', and the path to the file becomes the URL path.
In a way, this is similar to building websites using HTML or PHP files. Instead of writing HTML you write JSX and use React Components.


### Link Component

When linking between pages on websites, you use the `<a>` HTML tag.
In Next.js, you use the `Link` Component from `next/link` to wrap the `<a>` tag. 
`<Link>` allows you to do client-side navigation to a different page in the application.

The `Link` component is similar to using `<a>` tags, but instead of `<a href="…">`, you use `<Link href="…">` and put an `<a>` tag inside.
  
### Using `<Link>`

First, open pages/index.js, and import the Link component from next/link by adding this line at the top of the page:
```javascript
  import Link from 'next/link'
```

Then instead of doing this:
```javascript
<h1 className="title">
  Learn <a href="https://nextjs.org">Next.js!</a>
</h1>
```

Do the following:
```javascript
  <h1 className="title">
  Read{' '}
  <Link href="/posts/first-post">
    <a>this page!</a>
  </Link>
</h1>
```


###### `{' '}` adds an empty space, which is used to divide text over multiple lines.


### Client-Side Navigation

The `Link` component enables client-side navigation between two pages in the same Next.js app
Client-side navigation means that the page transition happens using JavaScript, which is faster than the default navigation done by the browser.

### Code splitting and prefetching

Next.js does code splitting automatically, so each page only loads what’s necessary for that page. That means when the homepage is rendered, the code for other pages is not served initially.
This ensures that the homepage loads quickly even if you have hundreds of pages.
Only loading the code for the page you request also means that pages become isolated. If a certain page throws an error, the rest of the application would still work.
Furthermore, in a production build of Next.js, whenever `Link` components appear in the browser’s viewport, Next.js automatically **prefetches** the code for the linked page in the background. By the time you click the link, the code for the destination page will already be loaded in the background, and the page transition will be near-instant!

Next.js automatically optimizes your application for the best performance by code splitting, client-side navigation, and prefetching (in production).
You create routes as files under `pages` and use the built-in `Link` component. No routing libraries are required.

> **Note:** If you need to link to an external page outside the Next.js app, just use an <a> tag without Link.
>
> If you need to add attributes like, for example, className, add it to the a tag, not to the Link tag
  
### Data Fetching

There are multiple ways to do data fetching with Next.js, this allows you to render your content in different ways depending on your application's use case. 
These include the following
- Pre-rendering with **Server-side Rendering**
- **Static Generation**
- Updating or creating content at runtime with **Incremental Static Regeneration**


#### SSR: Server-side rendering

This method requires server (node.js and npm)
#### SSG: Static-site generation

This method does not require server since Next.js will export all data as static pages
#### CSR: Client-side rendering

This method requires server (node.js and npm)
#### Dynamic routing 

#### ISR: Incremental Static Regeneration
**ISR** allows content editors and developers to use static generation on a per-page basis and update content without having to rebuild the entire site
Next.js generates new pages and regenerates current pages on the fly when data is updated
- **Note** there is no change on the first visit after the content is changed
-  **Note** the page visit triggers Next.js to re-fetch the page data in the background
- You will need to visit the page and then refresh to see the updated data

This method requires server (node.js and npm)
#### To automatic deploy Next.js web app to GitHub pages, follow this tutorial

This tutorial is based on exporting the web app to static pages. 
https://www.youtube.com/watch?v=yRz8D_oJMWQ&t=525s


#### Another tutorial for deploying next.js to firebase
https://github.com/jthegedus/firebase-gcp-examples/tree/main/functions-nextjs

  
### Best Place to put the nav in Next.js is in the app page (`_app.js` file)
  

### Each item in the array you create dynamicly is unique
```javascript
  <div>
        {blogPosts.map((item) => (
          <div key={item.slug}>
            <h1>{item.title}</h1>
            <p>{item.date.toString()}</p>
            <p>{item.content}</p>
          </div>
        ))}
      </div>
  
```
that is why we added `key={item.slug}`
  
  
### To render a collection of children, use an array

We use array to render a collection 
  
#### Unhandled Runtime Error
```error
Error: Hydration failed because the initial UI does not match what was rendered on the server.
Error: Text content does not match server-rendered HTML.
Error: Hydration failed because the initial UI does not match what was rendered on the server.
Error: There was an error while hydrating. Because the error happened outside of a Suspense boundary, the entire root will switch to client rendering.
```
I got all these errors because of one simple thing
To convert the date in html, intead of `toString()` it should be `toDateString()` 
Change it from this
```javascript
  <p>{item.date.toString()}</p>
```
  
To this
```javascript
  <p>{item.date.toDateString()}</p>
```
  
  
#### For adding stuff in html
 
We use the characters 
```
  ` `
```
