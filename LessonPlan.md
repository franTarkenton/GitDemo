# Agenda as identified in GIST

[link to the gist](https://gist.github.com/franTarkenton/ae3652cd38f126de2c8799b3aac4e394)

# Lesson Topics for today:

### Background 
 - Where might GIT help GeoBC, libraries? Projects? etc
 - Potential issues, separation of useful generic code from very specific project related code
 - Even on projects, one way to provide transparency.
 - Git Backgrounder?
 
 - If you can think of it, Git can probably do it!  Use the GOOGLE?
 - GIT is a vast topic!  This is only an introduction to hopefully get you 
   started / more comfortable with the tool conceptually.

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

Now we will do the same thing in eclipse:
 - Create or identify an existing project that you want to create git repository 
   around
 - Right click on the repository
 - Choose Team->Share
 - Check the box next to "Use or create repository in root folder of project"
 - Then select the option that gives you the directory for the project (usually 
   its the only option"
 - Click 'finish'
 
Now if you go to that directory you will see that there is a .git folder in there.
    
### Mechanics of Commits

- Repositories are made up of a bunch of commits.
- Commits are savepoints, saved states of your project.
- Commits can be labeled to make them easier to find and use.

Creating a Commit Using Command Line:
 - Create a file
 - Add the file to "staging"
     `git add <somefile>`
 - Commit the file
     `commit -m "this is my commit damn it`
     
 - Now after you have added this file to your repository you can also auto commit
   for changes using:
  
    `commit -a -m 'auto commit demo'`
    
Now same thing in eclipse:
 - To add the file to the list of files that are tracked by git, either find 
   the file in the eclipse "pydev package explorer", or open the file.
 - right click on the file and choose: team->Add to Index
 - to commit the file right click on the project and choose: Team->Commit
   this will open a git staging window, check that the files you want to commit
   are listed in 'staged Changes', then add a commit message.

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
      - origin is the short name that you can use to refer to this repo
      - you can name it anything you want.
      - By default git conventions suggest your upstream repo should be
        named origin, where upstream means the version that you are '
        contributing to / building.
      - There may be other remotes that you want to pull from, but not 
        necessarily contribute to.  You can add these to your project 
        also, and name them something else.
        
- 'Push' our code to the remote:
      `git push origin master`
      
- push: the git operation we are performing
- origin: the short name of the remote we are pushing to, could also spell out 
          the remote name
- master: the name of the local branch we are pushing. (more on branches to come)

Steps that May take place that illustrate the benefit of a remote:
1. you create a new git create repository.
2. add some code to the new repo
3. add files to the git repo (stage/commit)
4. create remote a repository.
5. push the code to the remote.
6. Share the remote url with team.
6. ian clones the remote on his local machine
7. ian makes changes, commits, and pushes (save changes to the remote)
8. I make changes
9. I commit my changes  (local)
10. Push my changes 
11. will be rejected
12. you are forced to look at the changes that Ian made and make a decision around
    what change is the correct one, and label the conflict as resolved.
    
* Also note, this scenario is simplified, ideally the "autoritative copy" of the 
repo would have been forked by Ian!

* Forking is part of next part.

### Contributing to a Remote:
These steps review what was covered in the session:

1. Login to github
1. Go to https://github.com/bcgov/dbc-pylib, and fork the repo.
1. Clone the forked version of the repo you just created:
   `git clone <path to repo>`
1. The clone will remember the relationship to the repo from which it was created
   example: `git remote -v`
1. Now import the project using eclipse (or whatever system you want to use)
1. Make some changes to the project, and commit.
1. Push the changes to the fork,
1. View the changes in the fork, on github.
1. View that the changes are not in the original version that we forked FROM
    - Also view the github visual on the status of the fork.
1. Issue a pull request
1. Merge the pull request.
1. view that they are the same.


[Another demo on what we covered here in forking](https://guides.github.com/activities/forking/)


Best practice is: fork, then pull request!
- Do demo using DataBCPyLib
- https://github.com/bcgov/dbc-pylib

