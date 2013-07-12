# threadsuitejobs.com

The ThreadSuite product & engineering jobs micro-site, based on [jekyll](http://jekyllrb.com/).

## Set up

```bash
git clone git@github.com:ThreadSuite/threadsuitejobs.com.git
cd threadsuitejobs.com
bundle
```

That's it.

## Editing the site

Editing the site and its content is a breeze if you use:

```bash
jekyll serve --watch
```

Jekyll will watch for changes and regenerate the site in the background.

### How do I change the home page?

The [index page](index.html) largely consists of includes, one for each section. You can find these files in the [_includes/ directory](_includes/).

### How do I add or change a team member's bio?

The team bios are in the front-matter of the [index page](index.html). Make your changes there. (And make sure it's valid YAML.)

The team images are in the [img/ dir](img/).
