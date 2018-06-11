# Agenda as identified in GIST

[link to the gist](https://gist.github.com/franTarkenton/ae3652cd38f126de2c8799b3aac4e394)

# Lesson Topics:

### Background 
 - Where might GIT help GeoBC, libraries? Projects? etc
 - Potential issues, separation of useful generic code from very specific project related code
 - Even on projects, one way to provide transparency.
 - Git Backgrounder?
 
 - If you can think of it, Git can proably do it!  Use the GOOGLE?
 - GIT is a vast topic!  This is only an intro to hopefully get you started / more comfortable 
   with the tool conceptually.

### What is GIT
 - Overview 
 - How git differs from centralized source code management systems like (SVN)
 - Git is not GitHub, GitHub is GIT
 - Other services (gogs/gittea)
 
### Getting started - ( Repository )

- What is a repository?  Container?
- Local vs Remote repositories

 - Create a repository
    - local first or remote first?
    
 - Local first
    - command line:
    
    ```
    # go to directory
    cd somedir
    git init
    ```

now take a look in the directory and see what the git magic has done

- Now we will do the same thing in eclipse!
    
### Mechanics of Commits

- Repositories are made up of a bunch of commits.
- Commits are savepoints, saved states of your project.
- Commits can be labelled to make them easier to find and use.

Creating a Commit:
 - Create a file
 - Add the file to "staging"
     `git add <somefile>`
 - Commit the file
     `commit -m "this is my commit damn it`
     
- Now after you have added this file to your repository you can also auto commit
  for changes using:
  
    `commit -a -m 'auto commit demo'`
    
- Now same thing in eclipse.

### Viewing Commits
- To list commits:
   `git log`
   
- To go to an old commit:
   `git checkout <commit id / or tag>`
   
- Same thing in eclipse:
   - Right click on project
   - select 'Team'
   - Show in history

### Remotes
- What is a remote?
- Remotes are a way of sharing!
- Remotes a copy of a repository, and a place where multiple people can work.

- Getting code to a remote:
   - A Create a remote on github (pressing buttons):
   - Link the local repo with the remote
     `git remote add origin <path to remote>`
   - origin:
      - origin is the shortname that you can use to refer to this repo
      - you can name it anything you want.
      - By default git convensions suggest your upstream repo should be
        named origin, where upstream means the version that you are '
        contributing to / building.
      - There may be other remotes that you want to pull from, but not 
        necessarily contribute to.  You can add these to your project 
        also, and name them something else.
        
- 'Push' our code to the remote:
      `git push origin master`
      
- push: the git operation we are performing
- origin: the shortname of the remote we are pushing to, could also spell out 
          the remote name
- master: the name of the local branch we are pushing. (more on branches to come)

- 

### Contributing to a Remote:

- Login to github
- To demo forking will look at [Will Burts burn severity scripts](https://github.com/bcgov/burn-severity)
  - fork as demo.
  
- Will delete fork franTarkenton/Data-BC-PyLib, and recreate!

1. Fork the github repo: https://github.com/bcgov/dbc-pylib
2. Clone the remote fork:
   `git clone <path to repo>`
3. The clone will remember the relationship to the repo from which it was created:
   `git remote -v`
4. Now import the project using eclipse
5. Make some changes to the project, and commit.
6. Push the changes to the fork, 
7. View the changes in the fork
8. View that the changes are not in the original version that we forked FROM
    - Also view the github visual on the status of the fork.
9. Issue a pull request
10. Merge the pull request.
11. view that they are the same.


[Another demo on what we covered here in forking](https://guides.github.com/activities/forking/)


Best practice is: fork, then pull request!
- Do demo using DataBCPyLib
- https://github.com/bcgov/dbc-pylib



 
   











 - Remote First
    - Create github account
    - press the buttons
 
   


Some basic Git Concepts
Repository
Commit
Staging
Remote vs Local repo
Fetch / Push / Pull
Working with Local Repository
Working with Remote Repositories
Best practices (fork / pull requests)
Thinking will do a demo showing how to do most of these things in Eclipse as well as from the commandline.

