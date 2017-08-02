---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE0NywiY29udGVudF90eXBlIjoiTGVzc29uIn0.SSzM-ySQEzpsvdtc07HTmONiKA0HYJCRALNcxm3YUJs

title: >-
  Git and Github
description: >-
  The basics of Git and Github
---
## What is Git?
- Git is a way for us to keep track of changes over time
- Git allows you to "time travel". You can go backwards in time to see what your code looks like.

## What is Github
Github is a git repository hosting tool that provides a web-based interface. It provides version control and collaboration features. 

## How does Github work
- **Repositories:** Usually used to organize a single project. This includes all of your folders, files, and assets. You always need to make sure your repository on Github is linked to your local project directory. 
- **Branches:** Branching is the way to work on different versions of a repository at one time. The default branch is the `master` branch. 
- **Making and Committing Changes:** Saved changes are called commits and each commit has an associated commit message, which is a description explaining the changes.
- **Pull Requests:** When you open a pull request, you’re proposing your changes and requesting that someone review and pull in your contribution and merge them into their branch. This is how collaboration works. 
- **Pushing and Merging:** This brings all your changes together into the Github repository.

## Github Workflow
First, create a repository on Github and follow the instructions to link it to your local machine. 

Follow these steps to commit changes as you work:
1. `git add .` - adds all changes to be "staged"
2. `git status` - make sure your changes have been added
3. `git commit -m "clear, concise, and descriptive commit message goes here"` - add a commit message to describe your changes
5. `git push origin master` - push your changes to the remote repository on Github
    
