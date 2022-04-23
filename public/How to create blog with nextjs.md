# Create a blog with Next.js

In this tutorial, we will create a blog with Next.js, Tillwind and Markdown. 
This will be a system to add articles as `md` files and generate static files for all the pages and articles created

#### As of right now, I am following the following tutorial:
Part1: https://www.youtube.com/watch?v=vu9gPcPs3mY&t=1084s
Part2: https://www.youtube.com/watch?v=hN9oO7M1LBQ
Part3: https://www.youtube.com/watch?v=gQIv-biWxjo


This is tutorial is based on multiple steps

## Create Data

The data are basicly the blog posts. We wil create a folder called `lib` and store the "blog posts" `md' files in it


## Create a templte for each blog post page
> Note: we use `[name].js` brackets for dynamic files. 
We create a folder called `blog` inside the `pages` folder. Then we create a `js` file and we call it `[slug].js` 
This we way whenever we go to this file, the name of changes based on the slug of the article we click on
We create a function inside the `[slug].js` file and we call it `BlogPage`
This function receives the desired data for the blog post, such as the title, date, auther, content, ...etc

