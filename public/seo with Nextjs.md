# SEO in Next.js

SEO  is one of the top reasons of using Next.js

If you are familiar with creating a regular single page application, whether with React or Vue or anything else, usually you get the initial load as html without the data. And then when your JavaScript loads and then your entire front end user interface is displayed in the browser. 

This is problematic for SEO. The search engine crawlers, only see an empty page. 
They don't see the content because the JavaScript is then loaded after.

It starts by loading an empty div and then wait for the JavaScript to load the content.

There are ways to get around this issue without using Next.js. However, the good thing about Next.js is because its built it in with it.
Its because the page is rendered on the server. Its server side generated. So its able to load the actual content. 
Or at least the website can be generated as static files.
