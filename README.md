# Git Workflow and Commands

Though there are 1000’s of articles about git, I have written this article is in order to document what I understood and how I understood which may help others as well.

# Find me if you wish

> If you think that these can be improved in anyway, please do suggest. Pull Request are highly appreciated. Find me if you wish [@Saif(https://www.linkedin.com/in/saif-aust-cse/).

## Workflow
 
   <div  style="text-align: center;">
       <img src="https://github.com/saifaustcse/Git-workflow-and-commands/blob/main/images/workflow.png" width="750" height="450">
   <div>

## Commands

### Configuration
   
   Git config that lets you get and set configuration variables that control all aspects of how Git looks and operates.

    # Display the current Git configuration.
    $ git config --list

    # Set the user information when submitting code.
    git config --global user.name "Saiful Islam"
    git config --global user.email "saifaustcse26@gmail.com"

    # Check
    git config --global user.name
    git config --global user.email


### Manage Repository

   Create a Repository in git hub/git lab then Clone the Repository
   * [How to create git hub repository.](https://docs.github.com/en/free-pro-team@latest/github/getting-started-with-github/create-a-repo)

    # Download an existing git repository to your local computer with its entire code history.
    $ git clone [url]

       
### Adding files and folder (Workspace --> Staging)

    # Add the specified file from the current directory to the staging.
    # Start tracking an untracked file
    $ git add [file1] [file2] [fileN]

    # Add the specified directory from the current directory to the staging, including subdirectories.
    # Start tracking an untracked directory
    $ git add [dir]

    # Add all files (tracked or untracked) from the current directory to the staging.
    # Start tracking a untracked file
    # Update the changes of tracked file from the current directory to the staging.
    $ git add .

### Commit changes (Staging --> Repository)

    # Submit the code from the staging to the Repository with a message
    $ git commit -m [message]

    # Submit the specified file from the staging to the Repository.
    $ git commit [file1] [file2] [fileN] -m [message]

    # Display all diff information when submitting.
    $ git commit -v

### Commit changes (Workspace --> Staging --> Repository)

    # Submit the changes of all tracked files after the last commit.
    $ git commit -am [message]

    # For untracked file
    $ git add .
    $ git commit -am [message]

### Remote synchronization from Repository(Repository --> Remote)

    # Push the current branch to the Remote Repository.
    $ git push origin [branch]

### Repository synchronization from remote (Repository <-- Remote)

    # Download specific branch.
    $ git fetch origin [branch]

    # Download all remote branches.
    $ git fetch --all

### Workspace synchronization from Repository (Workspace <-- Repository)

    # merge the specified branch to the current branch.
    $ git merge [branch]

    # merge a branch into a target branch
    $ git merge [source branch] [target branch]
        
### Workspace synchronization from remote (Workspace <-- Repository <-- Remote)

    # Retrieve the changes to the Remote Repository and merge with the local branch (fetch+merge)
    $ git pull origin [branch]

### Branching

    # List all local branches. (the asterisk denotes the current branch)
    $ git branch

    # List all remote branches.
    $ git branch -r

    # List all local branches and remote branches.
    $ git branch -a

    # Create a new branch, but still stay in the current branch.
    $ git branch [branch-name]

    # Create a new branch and switch to the branch.
    $ git checkout -b [branch]

    # Switch to the specified branch.
    $ git checkout [branch-name]

    # Switch to the previous branch.
    $ git checkout -

    # Delete the branch.
    $ git branch -d [branch-name]

    # Delete the remote branch.
    $ git push origin --delete [branch-name]
    $ git branch -dr [remote/branch]
        
### Inspection

    # Display the changed files.
    $ git status

    # Display the version history of the current branch.
    $ git log

    # Display all commits (Custom Filtering)
    $ git log --all

    # Display the 5 most recent commits (Custom Filtering)
    $ git log -5

    # View Commit History in ASCII Graph
    $ git log --graph

    # Display Just One Line Per Commit
    $ git log --oneline

    # Display Just One Line Per Commit with message (Custom Formatting)
    $ git log --pretty=oneline

    # Display all the users who have committed, sorted by number of commits.
    $ git shortlog -sn

    # Show the latest commits of the current branch.
    $ git reflog

  For more details:

   * [The-official-Git-site](https://git-scm.com/book/en/v2/Git-Basics-Viewing-the-Commit-History)
   * [Atlassian](https://www.atlassian.com/git/tutorials/git-log)
   * [Thegeekstuff](https://www.thegeekstuff.com/2014/04/git-log/)


### Discard changes from Workspace

    # Discard changes from the specified file of the Workspace.
    $ git checkout [file]

    # Discard all changes of the Workspace.
    $ git checkout .

### Revoke/Undo from Staging (Workspace <-- Staging)

    # If unwanted file were added to the staging area but not yet committed.
    # Restore specified file from the Staging to the Workspace.
    # Changes will stay in workspace. 
    $ git reset [file]

    # Restore all files from the Staging to the Workspace.
    # Changes will stay in workspace. 
    $ git reset
    $ git reset HEAD .

    # Restore all files from the Staging to the Workspace.
    # All chnages will be discard.
    $ git reset --hard

### Revoke/Undo from Repository (Workspace <-- Staging <-- Repository)

    # Restore all files from the Repository to the Workspace.
    # All changes will stay on Workspace.
    # Undo the last commit.
    $ git reset HEAD~1
    $ git reset --mixed HEAD~1

    # Restore all files from the Repository to the Staging.
    # All changes will stay on Staging.
    # Undo the last commit.
    $ git reset --soft HEAD~1

    # Restore all files from the Repository to the Workspace.
    # All chnages will be discard.
    # Undo the last commit.
    $ git reset --hard HEAD~1
 
### Revoke/Undo from Remote (Workspace <-- Staging <-- Repository <-- Remote)

    # Create a new commit to undo the specified commit.
    # All changes of the latter will be offset by the former and applied to the current branch.
    $ git revert [commit]
  
### Removing files or folders (Workspace --> Staging --> Repository --> Remote)
   
    # Manually delete the files or folders from Workspace
    # The following command will permanently remove the file
    $ git add .
    $ git commit -m "message"
    $ git push origin [branch]
        
### Stash

    # Temporarily saves or stashes changes of working copy and and move them in later.
    $ git stash

    # Saving Stashes with the message
    $ git stash save "<Stashing Message>" 

    # Check the Stored Stashes
    $ git stash list  
    
    # Restored the changes of latest stash from stashes
    # Remove the latest stash from stashes
    $ git stash pop

    # Restored the changes of latest stash from stashes
    $ git stash apply 
  
    # Restored the changes of specific stash from stashes
    $ git stash apply <stash id>

    # Remove the latest stash from stashes
    $ git stash drop

    # Remove the specific stash from stashes
    $ git stash drop <stash id> 

    # Remove all stashes
    $ git stash clear

### Tag

     # List all tags.
     $ git tag

     # Create a new tag in the current commit.
     $ git tag [tag]

     # Create a new tag in the specified commit.
     $ git tag [tag] [commit]

     # Delete the local tag.
     $ git tag -d [tag]

     # Delete the remote tag.
     $ git push origin :refs/tags/[tagName]

     # View the tag information.
     $ git show [tag]

     # Commit the specified tag.
     $ git push [remote] [tag]

     # Commit all tags.
     $ git push [remote] --tags

     # Create a new branch pointing to a certain tag
     $ git checkout -b [branch] [tag]


### Others

      # Select a commit to be merged into the current branch.
      $ git cherry-pick [commit]

      # Generate a archive for releasing.
      $ git archive


### Checkout vs Reset vs Revert

  * [Atlassian](https://www.atlassian.com/git/tutorials/resetting-checking-out-and-reverting)
  * [Medium](https://medium.com/@manivel45/git-merge-vs-rebase-reset-vs-revert-vs-checkout-dd5674d0e18a)
  * [opensource](https://opensource.com/article/18/6/git-reset-revert-rebase-commands)

### Merging vs. Rebasing

 * [Atlassian](https://www.atlassian.com/git/tutorials/merging-vs-rebasing)


# References

   I have followed many articles but among them, the following articles are really helpful. Those articles helped me a lot and also encourage me to write this article according to my understanding.
 
   * [The-official-Git-site](https://git-scm.com/book/en/v2)
   * [Atlassian](https://confluence.atlassian.com/bitbucketserver/basic-git-commands-776639767.html)
   * [Git-most-frequently-used-commands](https://medium.com/analytics-vidhya/git-most-frequently-used-commands-9df9f200c235)
   * [Ercankaracelik](https://ercankaracelik.wordpress.com/2018/12/08/basic-git-commands/)
   * [Tutorialdocs](https://www.tutorialdocs.com/article/git-basic-command-list.html)

