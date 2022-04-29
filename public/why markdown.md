Now, as far as you know why you might want to use markdown in a personal blog, you might think of

something like WordPress where you have, you know, an admin area.

You log in, you have a busy week editor with buttons to create headings and bold text and all that.

And that's fine.

But that gives you a lot of overhead.

And you have to if you're not using something premade like WordPress, you have to build all that functionality

yourself.

Markdown down gives you a much easier option.

And it's very fast.

It's portable.

So if you decide to move those articles to a different website or whatever, create a presentation from

them or emails, it's portable and you can just take those markdown files and do what you want with

them.


But before we move on, I just want to talk a little bit about front matter.

So when you have something like a blog post, you're going to need different fields right near the title.

We're going to have a date, an excerpt, a cover image, a category and author.

So we want these different fields and we're not using a database.

So they're not going to be database fields.

That's what front matter comes in.

And we can essentially just define our front matter at the top of the file and then have our post underneath

with the markdown format formatted syntax.

Now, as far as parsing the front matter, we're going to use this package here called Grey Matter so
