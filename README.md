## Using the ThreadSuiteJobs.com Staging Repository
### Step 1: Cloning gh-pages branch
You only need to do this once so long as you keep the /webExamples/ directory.
 > Clone the gh-pages repo to your local computer if you haven't already.
 > I choose to clone the gh-pages repo, which is set as the the default branch, INSIDE the _site directory of the master branch as it is ignored and nearby.
(eg. **/ThreadSuiteJobs.com/_site/webExamples/**)

__If having a repo inside a repo makes you uncomfortable, just choose a different location__

```bash
cd /threadsuitejobs.com/_site/
git clone https://github.com/pro3d/webExamples.git
```
NOTE: The gh-pages branch on my Pro3d account is set as the default branch; I do not use the master branch; **Treat it like the webroot of a ftp server, however, the CNAME file from Production MUST BE REMOVED or it will cause an error**

### Step 2: Edit & Commit to Production
#### Make your edits inside the ThreadSuiteJobs.com master branch, then test locally
```bash
jekyll serve --watch
```
 >Browse to [http://localhost:4000](http://localhost:4000) to test changes.

##### Sync & Commit to push final changes out to threadsuitejobs.com master branch when done editing.

### Step 3: Copy Jekyll Build
#### I find it quickest to locally copy all files of your latest Jekyll build & overwrite the contents within /_site/webExamples/ from Step 1.
NOTE: Remember that these files do NOT check into the master branch; they are simply compiled output from the master branch.

### Step 4: Edit CSS/JS Paths on gh-pages branch
#### Files to modify:
(There are currently only 4 filepaths to change in the head of each file, 3 for css & 1 for a html5shiv.js include)
 >1. /_site/webExamples/index.html
 >2. ALL .html job listings in each of the /_site/webExamples/2013/MM/DD subdirectories
NOTE: Since we are essentially cloning a repo cross-domain, a well documented weakpoint of Jekyll at the moment, these irritating edits are sadly required.

How you edit these is up to you, locally via text editor OR use built in Edit Button on Github.com... **IF you don't mind pushing broken links to Staging while you're fixing them**
```bash
CHANGE ALL INSTANCES OF href="/css/fileName.css" AND href="/js/fileName.js" TO href="/webExamples/css/fileName.css" AND href="/webExamples/js/fileName.js" to match the gh-pages path.
```
### Finally: Sync & Commit then Push gh-pages branch to Staging at [Pro3d.Github.io/webExamples](http://pro3d.github.io/webExamples)

#### I will employ a much more elegant solution ASAP, as there are hacks and tricks to make this more STREAMLINED... but I need to make the time.
