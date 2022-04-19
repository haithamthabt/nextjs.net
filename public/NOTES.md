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
  - 'pages/index.js' is associated with the '/' route.
  - 'pages/posts/first-post.js' is associated with the '/posts/first-post route'
  
  
#### To can create different pages in Next.js.
Simply create a JS file under the 'pages directory', and the path to the file becomes the URL path.
In a way, this is similar to building websites using HTML or PHP files. Instead of writing HTML you write JSX and use React Components.


### Link Component
When linking between pages on websites, you use the <a> HTML tag.
In Next.js, you use the Link Component from next/link to wrap the <a> tag. 
<Link> allows you to do client-side navigation to a different page in the application.
  
### Using `<Link>`
First, open pages/index.js, and import the Link component from next/link by adding this line at the top:
```javascript
  import Link from 'next/link'
```
