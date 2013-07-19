# ThreadsSiteJobs.com Staging Repository

## Step 1: Clone Me

 > Clone THIS gh-pages repo:
```bash
jekyll serve --watch
```

NOTE: The gh-pages is not a picture of the master branch, rather it is treated like the webroot of a ftp server.

## Step 2: Editing the site, or...
### Just pasting in contents of the ThreadSuiteJobs.com _site directory following a Jekyll build)

Since there is a difference in directory naming, we must manually edit the CSS Path Structure:

```bash
jekyll serve --watch
```

Jekyll will watch for changes and regenerate the site in the background.

### How do I change the home page?

The [index page](index.html) largely consists of includes, one for each section. You can find these files in the [_includes/ directory](_includes/).

### How do I add or change a team member's bio?

The team bios are in the front-matter of the [index page](index.html). Make your changes there. (And make sure it's valid YAML.)

The team images are in the [img/ dir](img/).
