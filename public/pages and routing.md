# Pages & Routing in Next.js

If you are familiar with react `create-react-app`, if you want to create a route, you will have to install a third party  package like `react-router-Dom`

In Next.js we dont have to do that. We dont have to define our routes manually in our code.  All we have to do is put a react component into the `pages` folder

To create a react component. Lets for example create a new page.  Lets call it `about.js` and simply create a react component inside it.

> Note: You don't want to import `React` to create react components in Next.js

> Note:  The convention I'm going to use for page component names is going to be uppercase, whatever the page name and then page **`AboutPage`**

```javascript
export default function AboutPage() {
  return (
    <div>about</div>
  )
}
```
Now if you go to `localhost:3000/about`, you will get the about page.  It just works.  That's the beauty of Next.js


#### Nested Routes

To create nested routes similar to `localhost:3000/blog/my-blog-post` , all we need to do is to create a folder named `blog` inside the `pages` folder, and then create a dynamic post file to work for all the posts.  Lets create one but we will name it `[slug].js` 
Note that we have `[]` for the slug file so that Next.js can understand that this is dynamic file and it will be named based on the slug "the post url"

> Note, we can have an `index.js` file inside the `blog` folder so it can be accessed from the blog url `localhost:3000/blog`

