Slidedeck: HTML5 Slideshows in markdown
---------------------------------------

### [Take a look at these slides!](http://htmlpreview.github.io/?https://github.com/rmcgibbo/slidedeck-example/blob/master/index.html)


Overview
========

This is a repackaging of the google io 2012 slidedeck, with [these](https://github.com/francescolaffi/elastic-google-io-slides) modifications, to be a little easier to use and more suitable for scientific presentations.

We've made a few changes:

- You edit and author your entire presentation in markdown.
- All the metadata about your project is set within the markdown file, including things like
  the title and author.
- It's packaged as a python project.
    - You run `slidedeck create` to make a new deck. This will create a new directory with your
      project. In particular, there will be a fine in there called `slides.md` that contains the
      markdown source for your slides.
    - `slidedeck render` will render your deck from markdown to html5.
    - `slidedeck watch` will watch your project and rerender the slides whenever you change the
       content (useful for iterative development).
- I made a few stylistic changes to the css, including changing the font size.
- The slides can contain LaTeX, which is rendered via mathjax.
- There are no google logos all over the place


Getting started
===============
- Install the package with `python setup.py install`. This will add the command
  line program `slidedeck` to your PATH.
- Create a new project, complete with some template slides, the css, and the
  javascript with `slidedeck create my_slides`.
- Look in there for the `slides.md` file, and edit it to your liking.
- Compile the slides from markdown into html with `slidedeck render`
- If you'd like to autocompile your markdown any time the files change on disk, try
  using the command `slidedeck watch`.
- If you're curious about how any of these commands work, pass the `-h` flag to the
  command line executable, like `slidedeck -h` or `slidedeck create -h`
  
Dependencies
============

You will need a modern python installation (tested on 2.7) with
`jinja2` and `markdown` installed. To use the `slidedeck watch` command,
you'll also need `watchdog` installed.

You can get these packages with the `easy_install` or `pip` package managers
by running

```
sudo easy_install jinja2 markdown watchdog
```

or

```
sudo pip install jinja2 markdown watchdog
```

License
-------
```
            DO WHAT THE FUCK YOU WANT TO PUBLIC LICENSE
                    Version 2, December 2004

Everyone is permitted to copy and distribute verbatim or modified
copies of this license document, and changing it is allowed as long
as the name is changed.

            DO WHAT THE FUCK YOU WANT TO PUBLIC LICENSE
  TERMS AND CONDITIONS FOR COPYING, DISTRIBUTION AND MODIFICATION

0. You just DO WHAT THE FUCK YOU WANT TO.
```

