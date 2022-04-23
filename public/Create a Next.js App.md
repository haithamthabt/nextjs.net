# Create Your First Next.js App

You will need Node.js in your machine in order to create a Next.js app


### To Create the Next.js App
Run the following command

```shell
npx create-next-app my-app-name
```
That's going to set up all the default folders, files and dependencies for our next website in this folder.

Then we can `cd` into our project folder
```shell
cd my-app-name
```

Now we can test the default app by running the dev server
```shell
npm run dev
```

That should open up a landing page on `localhost:3000`

It's basically just a single page with some links to some outside documentation.

### Now lets go over what have in our project (The default files and folders)

Let's just go over some of these files and folders.

#### Lets start with `package.json` 

```json
{
  "name": "my-app-name",
  "version": "0.1.0",
  "private": true,
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "start": "next start"
  },
  "dependencies": {
    "next": "12.1.5",
    "react": "18.0.0",
    "react-dom": "18.0.0"
  }
}
```


There is not much in here.  For dependencies,  we just have Next, React, and React-Dom. For scripts, we have dev, build, and start. We we will explore more in up coming tutorials. 
- `dev` : to run the dev server
- `build` :  to create our production build
- `start` : to run your production build on your local machine

#### Lets now look at the folders
##### Public Folder

`public` folder, is for anything that is going to be directly accessible to the browser. Basically like your static folder images, style sheets, ...etc. 

##### Pages Folder

Basically this is where all of your pages will go. So for example index.js is your home page.
Now in Next.js pages are nothing more than a react component. So it's a functional component.

**`_app.js`**  Next.js uses an app component to initialize pages. 
if we look inside the `_app.js` we will find a function or we should call it a component. 

```javascript
function  MyApp({ Component, pageProps }) {
return  <Component {...pageProps} />
}
```
This component that's being returned is whatever the current pages. So if you go to the homepage, the return would be the homepage `pages/index.js` 
Also inside **`_app.js`** we put our common stuff that we need it to be on every page such as navbars
More about `_app.js` is on here (_app.js tutorial page)

##### Styles Folder
`styles` folder is dedicated for the style sheets files. 
As far CSS, there are many ways to do it. 
You can use the standard module system. But you could also use style components. You could use a framework like tailwind. You could put everything in the global success. So it's really up to you.

We are gonna use the module system for now. 
So basically the `globals.css` is being brought in to the `_app.js` file

```javascript
import '../styles/globals.css'

function MyApp({ Component, pageProps }) {
  return <Component {...pageProps} />
}

export default MyApp
```

**`globals.css`** is just some very basic global styling.

And then you have **`home.module.css`** this was imported into the homepage `index.js`
So the idea is to have specific stylesheets for specific pages and specific components, and they have to have this naming convention `pageName.module.css`

>Notes: `module.css` files have to be imported as styles as follows
```javascript
import styles from  '../styles/Home.module.css'
```
Therefor we **CANNOT** import it as global as follows
```javascript
import  '../styles/Home.module.css'
```

The only place you can import global stylesheets is in `_app.js`

More about styles on the (styles tutorial page)
