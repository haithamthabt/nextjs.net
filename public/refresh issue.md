# Refresh issue on Static Next.js Site

So we had the issue of getting 404 or getting to homepage when refreshing any page.
To fix this 
I just created next.config.js file and put the following in it

```
module.exports = {
    exportTrailingSlash: true,
  }
```

> Note: There were some code inside next.config.js and did not know where to put my code, when I added it to the bottom of file
> But when I deleted everything in the file and just added my code, then it worked.
