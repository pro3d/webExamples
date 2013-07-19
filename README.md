## ThreadsSiteJobs.com Staging Repository

### Step 1: Cloning
You only need to do this once so long as you keep the directory.
 > Clone THIS gh-pages repo if you haven't already.
```bash
git clone https://github.com/pro3d/webExamples.git
```
NOTE: The gh-pages is not a picture of the master branch, rather it is treated like the webroot of a ftp server.

### Step 2: Make your Edits Locally
#### Make your changes and test locally
```bash
jekyll serve --watch
```
 >Browse to localhost:4000 in browser to test changes.
##### Push final changes out to threadsuitejobs.com master branch.

### Step 3: Copy Jekyll Build

#### I find it quickest to locally delete all contents within the webExamples dir each time I update: YES, you read that right...LOL
... I then simply copy all files of the latest Jekyll build from your threadsuitejobs.com/_site directory, and push the gh-pages branch.

NOTE: We aren't doing anything with the master branch, since we already have everything in the ThreadSuite master branch.

SO, since we are essentially cloning a site cross-domain, a well documented weakpoint with Jekyll at the moment, we will manually edit any CSS Paths on .html pages.
These are the files we need to edit:

 >1. index.html
 > ... and ...
 >2. All job listings in the 2013 directory
How you edit these is up to you, locally, or actually clicking Edit on Github is just as fast if you don't mind pushing a broken test site for a few minutes.
```bash
CHANGE href="/css/blah.blah.css" to "href="/webExamples/css/blah.blah.css" to match the gh-pages path.
```
