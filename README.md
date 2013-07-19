## ThreadsSiteJobs.com Staging Repository
### Step 1: Cloning gh-pages branch
You only need to do this once so long as you don't delete the entire directory.
 > Clone the gh-pages repo to your local computer if you haven't already.
 > I choose to clone the gh-pages repo INSIDE the _site directory of the production site as it is ignored and nearby.
__If this makes you uncomfortable, just choose any location.__
(eg. **/ThreadSuiteJobs.com/_site/webExamples/**)
```bash
cd /threadsuitejobs.com/_site/
git clone https://github.com/pro3d/webExamples.git
```
NOTE: The gh-pages branch on my Pro3d account is not based on a master branch; **I just treat it like the webroot of a ftp server**

### Step 2: Make & Commit Changes to Master
#### Make your edits inside the ThreadSuiteJobs.com master branch, then test locally
```bash
jekyll serve --watch
```
 >Browse to [http://localhost:4000](http://localhost:4000) to test changes.

##### Commit and push final changes out to threadsuitejobs.com master branch when done editing.

### Step 3: Copy Jekyll Build
#### I find it quickest to locally copy all files of your latest Jekyll build & overwrite the contents within /_site/webExamples/ from Step 1.
NOTE: Remember that these files do NOT check into the master branch; they are simply compiled output from the master branch.

### Step 4: Edit CSS Paths on gh-pages branch
#### Files to modify:
(There are currently only 3 filepaths to change in the head of each file)
 >1. /_site/webExamples/index.html
 >2. ALL .html job listings in each of the /_site/webExamples/2013/MM/DD subdirectories
NOTE: Since we are essentially cloning a repo cross-domain, __a well documented weakpoint of Jekyll at the moment__, these irritating edits are sadly required..

How you edit these is up to you, locally via text editor, or you can click the Edit Button on Github.com;
**IF you don't mind pushing broken CSS links for a minute.**
```bash
CHANGE ALL INSTANCES OF href="/css/fileName.css" to href="/webExamples/css/fileName.css" to match the gh-pages path.
```
### Finally: Commit and Push gh-pages branch.

#### I will employ a much more elegant solution ASAP, as there are hacks and tricks to make this more STREAMLINED... but I need to make the time.
