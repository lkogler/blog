# The Pivotal Engineering Journal

Welcome to our little slice of the internets!  This blog is dedicated to technical (and cultural) posts by the Pivotal Engineering team.  If that's you, then *please*, *please*, *please* contribute!

[Live site](http://engineering.pivotal.io/) | [Issues](https://github.com/pivotal/blog/issues) | [Pull Requests](https://github.com/pivotal/blog/pulls) | [Hugo](http://gohugo.io/)

## Contributing

1. Fork this repository
1. Pull your fork, and [run it locally](https://github.com/pivotal/blog#running-locally), so you can see what you're writing.
1. [Write your post](https://github.com/pivotal/blog#writing-a-post).
1. Gather feedback from your engineering peers.  Iterate, repeat.
1. Ping `@pivotal/engineering-directors` when you feel it's ready for the world.

## Running Locally

This site uses [Hugo](http://gohugo.io) v0.14, which is easy to install:

~~~
$ brew install hugo
$ hugo version
Hugo Static Site Generator v0.14 BuildDate: 2015-06-16T21:41:12+01:00
~~~

After cloning this repository, navigate into the new directory, run `./bin/watch` in a terminal and then browse to [http://localhost:1313](http://localhost:1313) to see your local copy of the blog.

Hugo has [LiveReload](http://livereload.com/) built in, so if you have that configured in your browser, your window will update as soon as you make a change.  Hugo is *fast*, so you might not realize the reload has already happened.

## Writing a Post

1. Fork this repo to a copy you can push to.
1. Add yourself as an author (first time only, obvs.):

    ~~~
    $ cp ./data/authors/tammer.yml ./data/authors/bob.yml
    $ vi ./data/authors/bob.yml
    ~~~

1. Create a new draft post with `./bin/new_post name-of-post`.  This will create a new file at location `./content/post/name-of-post.md`. It's just markdown, and the template provides instructions on any advanced bits.  Be sure to change the metadata in the file's YAML front-matter -- one thing to change immediately is the `authors:` value should include the name of your author file (`bob` in the example above) in the list.

1. *Meta:* If you want to change the default new post template, it's in `./archetypes/post.md`.

## Publishing Your Copy

You can publish your fork to your own cf org by running `./bin/publish`.  That script will push your blog to `pivotal-cf-blog-$USER` (where `$USER` is your local unix username.  You'll need to make sure you've `cf target`ed the org and space you want to push to.

## Publishing to Production

It's all about PRs.  Submit your post as a pull-request, ping anyone else you like, gather feedback, iterate, etc.

Once the PR's ready, tell `@pivotal/engineering-directors`, and we can then publish by targeting our `pivotal` org and `blog` space, and then running `./bin/publish prod`.

## Changing the style

`./themes/pivotal-ui` is a port of the [Pivotal UI](https://github.com/pivotal-cf/pivotal-ui) project.  I basically copied the compiled css and image files over.  If you want to change the look of this site, then you should edit the templates in there.
