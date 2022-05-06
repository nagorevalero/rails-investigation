# Rails Demo: The First Fourteen Minutes

This code is taken from the first 14 minutes of the [Rails 7
Demo](https://www.youtube.com/watch?v=mpWFrUwAN88). It has been slightly
modified for learning purposes.

We will use this to help you learn a bit about Rails and how it works. In a
wider sense, you will also build your engineering skill of breaking down a
complex codebase, building a mental picture of how it operates, and then moving
forward with changes.

Start with [Quickstart](#quickstart), and then move on to the [Investigation
Exercises](#investigation-exercises).

## Quickstart

Clone this repository, and in its directory:

```shell
; bundle install # To install the dependencies
; rails db:setup # To set up the database
; rails test     # To run the tests
; rails server   # To start the dev server
# Now open http://localhost:3000/posts
```

## Investigation Exercises

On a course like ours, it can feel like you need to move very fast in order to
be successful. In the real world, it is important to take your time building
understanding of the code you're operating with. Racing ahead to add features
is fun, but it is poor engineering practice in the real world.

These exercises are small tasks for you to take your time with. Use them to
build an understanding of how this system works.


For diagrams, use something other people can see and refer to rather than a bit
of paper. For example, [Excalidraw](https://excalidraw.com),
[draw.io](https://draw.io/) or [miro.com](https://miro.com/).

### Challenge 1

Open up the web interface at `http://localhost:3000/posts`. Perform the
following tasks:

1. Add a new post
2. View a single post
3. Add a second post
4. View a list of both posts
5. Edit a post
6. Delete a post

### Challenge 2

Locate the `PostsController`. Create a diagram that describes which controller
actions were used in the sequence you did in Challenge 1. Here's a starter to
give you an idea:

```
      What I did                   Controller Methods

┌─────────────────────┐         ┌───────────────────────┐
│                     │         │                       │
│   Visited /posts    │         │ PostsController#index │
│                     │         │                       │
└─────────────────────┘         └───────────────────────┘
          │                                 │
          ▼                                 ▼
┌─────────────────────┐         ┌───────────────────────┐
│                     │         │                       │
│  Clicked 'New Post' │         │  PostsController#new  │
│                     │         │                       │
└─────────────────────┘         └───────────────────────┘
          │                                 │
          ▼                                 ▼
        ?????                             ?????
```

### Challenge 3

Add the phrase "Thank you for reading my posts!" to the bottom of every page.

Tip: if you are having trouble finding out where the views are, try doing a
global find (cmd+shift+f in VS Code) for a piece of text you see on the page.
For example: "Destroy this post".

### Challenge 4

Write a test that "Thank you for reading my posts!" appears on the `/posts`
index page.

Note: there are two potential test files to add this test to. Find both of them,
look at the kinds of tests they are, see which one you think is best to add your
test to.

### Challenge 5

If you look at the title of the tab in your browser, it says 'Demo'.

Change it to say 'Blog'.

### Challenge 6

Make a diagram that describes, to the best of your understanding, what happens
when the user adds a new post. Include requests, response, controllers,
templates, and the database.

You can have areas of uncertainty. Highlight those and see what you can learn
from reading the code about how they work.

### Challenge 7

Open up the Javascript console in your web browser. Usually this is cmd+opt+i.

Locate some Javascript files in the codebase. Add `console.log("Hello");` to
various places and refresh the page to see which of these files are running and
what parts of them get executed.

### Challenge 8 (Extra Challenge)

Take this one slowly. If it took you all day, or multiple days to do it, that
would be fine because you will go away with valuable knowledge.

Make a change to the app so that:

* Posts have a new field called 'cool'.
* The app can create posts with `cool` set to true or false.
* When the user visits `/posts/cool` they see a list of only the cool posts.
* When the user visits `/posts/uncool` they see a list of only the uncool posts.

Your job will require you to write tests, so write tests here.

## Beyond

If you'd like to keep building up the application, you can follow the steps DHH
takes in the video after 13:50.

## Thanks

To DHH for the code, and @ipepe-oss for extracting it.
