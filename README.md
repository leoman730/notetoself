## Note to Self [![Build Status](https://travis-ci.org/leoman730/notetoself.svg?branch=gh-pages)](https://travis-ci.org/leoman730/notetoself)

A blog for my reading reflections: [Note to Self]

Powered by [Jekyll] 3.x and [Jekyll Bootstrap].

```sh
# start a local server and watch files change
jekyll serve --incremental

# create a new post/page
rake post title="post title"
rake page name="about.md"
rake page name="pages/about.md"

# Install/switch theme
rake theme:install git="https://github.com/jekyllbootstrap/theme-the-program.git"

rake theme:switch name="the-program"
```
More info on [Jekyll Bootstrap Doc].


[Note to Self]: http://leoman730.github.io/notetoself
[Jekyll]: https://jekyllrb.com/
[Jekyll Bootstrap]: http://jekyllbootstrap.com/
[Jekyll Bootstrap Doc]: http://jekyllbootstrap.com/usage/jekyll-quick-start.html
