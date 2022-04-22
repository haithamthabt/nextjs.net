# Understanding different types of frontend app rendering

### Client-Side Rendering

This is the most common rendering strategy in React applications. All the render happens on the browser using JavaScript. The first load performance isn't great due to the browser having to download all static assets and then run a lot of JavaScript to render the page. However, there are less moving pieces and it’s easy to maintain and iterate on. If your app doesn’t necessarily need SEO or having a fast first page loading time, using client-side rendering might work well for you.

### Server-Side Render

This is probably the “oldest” rendering strategy and it’s the complete opposite of rendering everything in the browser. Instead, everything is rendered on a remote server. This way, the browser will download fully rendered HTML, which will make your page load way faster and is better optimized for SEO bots.

### Static Rendering

In the React ecosystem, this type of rendering was introduced by frameworks like GatsbyJS and Next.js. This one is similar to server-side rendering, but instead of generating the HTML on every request, it compiles everything beforehand on build time. It can be very useful for sites where the content doesn’t change that often, like documentation pages, or a corporate website.

### Static Rendering

In the React ecosystem, this type of rendering was introduced by frameworks like GatsbyJS and Next.js. This one is similar to server-side rendering, but instead of generating the HTML on every request, it compiles everything beforehand on build time. It can be very useful for sites where the content doesn’t change that often, like documentation pages, or a corporate website.

It’s also easier to maintain/deploy, because you don’t need to actually run a web server. Since everything is pre-rendered, uploading all your artifacts to a static hosting such as gethub pages or firebase is enough.

### Hybrid Rendering

This is the strongest point of Next.js: mixing client + static rendering or client + server rendering. There is no way to only have client-side rendering in a Next.js app.

With a hybrid approach, you can take advantage of both strategies. Serve pre-compiled HTML to the browser and then take advantage of  [React's hydration](https://www.gatsbyjs.com/docs/conceptual/react-hydration/)  on the client and have a fully interactive page with the exact same code.
