---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE1MCwiY29udGVudF90eXBlIjoiTGVzc29uIn0.05UWdzqhUCHfg6GM9aWKQ2YleByZHszzZGbl2kCS3mc

title: >-
  Github for Collaboration
description: >-
  Learning to use Github to collaborate
---
# Github Collaboration
If you don't already know, GitHub is an incredibly effective way to collaborate on development projects. Providing a place for anyone with an internet connection to have an avenue where they can share code with the world for free (not to mention the robust supporting tools for source inspection and easy viewing of commit histories). GitHub has been adopted by many large open-source projects as their primary home for collaboration and contribution.

There are many workflows that you can use to collaborate on Github, and this is a fairly common one. 

# All About Branches
Branches are used to develop features isolated from each other. The master branch is the "default" branch when you create a repository. When working in a collaboration manner, use other branches for development and merge them back to the master branch upon completion.

We have already been familiar with branches from `gh-pages`. That is a branch. You can make any other branches, specific to what you are working on. 

![branches](http://rogerdudler.github.io/git-guide/img/branches.png)

create a new branch named "feature_x" and switch to it using: 
`git checkout -b feature_x`

switch back to master:
`git checkout master`

and delete the branch again: 
`git branch -d feature_x`

a branch is not available to others unless you push the branch to your repository:
`git push origin <branch>`


# A Successful Workflow
- Set up your workflow at the onset of your projects
- Assign each person a branch or feature and make sure each person only works on those branches until you are ready to merge. 

1. Create the master branch on one person's account
2. Set up the base directory with all your pages and push to the master branch. For this project, it is probably good to have one Sass file and then a bunch of partials that you will each work off. No group member should we working on the same files!
3. Add the users as collaborators
4. Each user should now have read/write access to the repository and can `git clone` the master repository to their own machine
5. Create and switch to your feature/page branch
6. Work away (but only make sure you edit **YOUR** files)
7. To commit changes, push to your feature/page branch 
8. When you are ready to merge all of your changes, complete a pull request in github (we will discuss this on Monday)

Helpful tip: While collaboration, you will not push to the master branch until the very end. This is going to help us avoid merge conflicts. 
