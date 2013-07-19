# ThreadsSiteJobs.com Staging Repository

## Clone Me

 > Clone THIS gh-pages repo if you haven't already.
```bash
jekyll serve --watch
```

NOTE: The gh-pages is not a picture of the master branch, rather it is treated like the webroot of a ftp server.

## Editing the site
### I find it quickest to just delete all contents of the freshly checked out repo: YES, you read that right...LOL, then copy the contents of the latest Jekyll build from ThreadSuiteJobs.com/_site directory )

Since we are essentially cloning a site cross-domain, a well documented weakpoint with Jekyll at the moment, we will manually edit any CSS Paths on .html pages.
At this point, it just cosists of:
 >index.html
 >... and ...
 >any job posting html page in the 2013 directory
How you edit these is up to you, locally, or actually clicking Edit on Github is just as fast if you don't mind pushing a broken test site for a few minutes.
```bash
CHANGE href="/css/blah.blah.css" to "href="/webExamples/css/blah.blah.css" to match the gh-pages path.
```
