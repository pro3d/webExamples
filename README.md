## ThreadsSiteJobs.com Staging Repository
### Step 1: Cloning
You only need to do this once so long as you keep the directory.
 > Clone THIS gh-pages repo if you haven't already.
```bash
git clone https://github.com/pro3d/webExamples.git
```
NOTE: The gh-pages branch, in this case, is not a fork of the master branch, rather just treat it like the webroot of a ftp server.

### Step 2: Make your Edits Locally
#### Make your changes to the ThreadSuiteJobs.com master branch and test locally
```bash
jekyll serve --watch
```
 >Browse to localhost:4000 in browser to test changes before updating the production master branch content.
##### Commit and push final changes out to threadsuitejobs.com master branch when done editing.

### Step 3: Copy Jekyll Build to Pro3d
#### I find it quickest to locally copy all files of your last Jekyll build & overwrite the contents within the webExamples dir from Step 1.

... I then simply copy all files of your last Jekyll build from your threadsuitejobs.com/_site directory, and push the gh-pages branch.

NOTE: I am not even using the master branch, since we already have everything in the ThreadSuiteJobs.com master branch.

### Step 4: Manually Edit CSS Filepaths
#### Files to modify: (CSS paths are in the head of the file)
 >1. index.html
 >2. ALL .html job listings in the /2013/MM/DD subdirectories
NOTE: Since we are essentially cloning a repo cross-domain, a well documented weakpoint with Jekyll at the moment, these irritating edits are sadly required.

How you edit these is up to you, locally, or actually clicking Edit on Github.com is just as fast if you don't mind pushing broken CSS links for a minute.
```bash
CHANGE href="/css/blah.blah.css" to "href="/webExamples/css/blah.blah.css" to match the gh-pages path.
```

## I will work on a more elegant solution, as there are hacks and tricks to make this more STREAMLINED... but I need some more time.
