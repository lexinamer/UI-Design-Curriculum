---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE1MSwiY29udGVudF90eXBlIjoiTGVzc29uIn0.1ic39Xyky8sKBvNHMuU-Ej0YjQYC4yiWV5i_w9oPWvQ

title: >-
  Project Directories
description: >-
  The importance of setting up a project directory the right way
---
## What is a project directory
- In computing, a directory is a file system cataloging structure which contains references to other files and folders.
- The top-most directory in a filesystem, which does not have a parent of its own, is called the root directory.

## Why is this important
- When working with any project, especially ones that will published to the web, it is vital to have an organized and methodological structure to your directories. 
- Without this structure, it would be impossible to pass the project to someone else for collaboration, it is going to slow down your progress and eventually something will break. 

## Dev Project Structure
- The root directory should be the project name
- Inside the root should be two addl directories 
   - images
   - css
- All images and assets should **only** go into the `images` folder
- All stylesheets should **only* go into the `css` folder
- Any HTML pages should be at the top of the root directory 

![Directory](https://s22.postimg.org/t957550o1/Screen_Shot_2016_10_03_at_9_55_40_AM.png)

## Notes and Tips
- Find a naming convention and stick to it. 
- Lowercase and **NO SPACES** for any file and directory names
- The home page of your site must **ALWAYS BE** `index.html`
- Set up your directory before you do anything else on the project 
- Open up the entire directory in Atom when you are working. This will keep from making unnecessary errors. 
