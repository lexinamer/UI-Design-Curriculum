---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE0OSwiY29udGVudF90eXBlIjoiTGVzc29uIn0.cMfMYyuQvDIbk1uL_oE5pF-bzOzsTV6cSvMv23hbwr0

title: >-
  Github Pages
description: >-
  How to host your project on Github using Gh-Pages
---
## What is Github Pages?
GitHub Pages is a static site hosting service. GitHub Pages is designed to host your personal, organization, or project pages directly from a GitHub repository. 

## Publishing to Github Pages
1. In the command line, `cd` to your project folder and push to Github like normal: 
```
git add .
git commit -m "message"
git push origin master
```

2. When you are ready to publish to Github pages, create and switch to a new branch called gh-pages: `git checkout -b gh-pages` 

3. Merge your master files to the new branch: `git merge master`

4. Push to the new branch: `git push origin gh-pages`

5. Switch back to the master branch: `git checkout master`

> - Once you have created a gh-pages branch in step 2, when you go to push to gh-pages again, you need to only switch to the branch using `git checkout gh-pages`
> - Your URL is: username.github.io/reponame

[A Guide to Using Github Pages](https://www.thinkful.com/learn/a-guide-to-using-github-pages/)
