# Find me

> If you think that these can be improved in anyway, please do suggest. Pull Request are highly appreciated. Find me if you wish [@Saif(https://www.linkedin.com/in/saif-aust-cse/).

1. ### Workflow
 
    <div  style="text-align: center;">
          <img src="https://github.com/saifaustcse/SDLC_Methodologies/blob/master/images/workflow.png" width="500" height="300">
    <div>
     Here are some of the most important terms are:

       Workspace
       Index / Stage
       Repository
       Remote

2. ### Create a New Repository

       # Create a new Git repository in the current directory.
       $ git init
       
       # Create a new directory and initialize it to the Git repository.
       $ git init [project-name]
       
       # Download a project and its entire code history.
       $ git clone [url]


3. ### Configuration
    The setting file for Git is .gitconfig, which can be placed under the user's home directory (global configuration) or under the project directory (project configuration).

       # Display the current Git configuration.
       $ git config --list
      
       # Edit Git Configuration File.
       $ git config -e [--global]
       
       # Set the user information when submitting code.
       $ git config [--global] user.name "[name]"
       $ git config [--global] user.email "[email address]"

4. ### Add/Delete Files

       # Add the specified file to the Index.
       $ git add [file1] [file2] ...

       # Add the specified directory to the Index, including subdirectories.
       $ git add [dir]

       # Add all the files in the current directory to the Index.
       $ git add .

       # Delete the files in the Workspace and put this deletion into the Index.
       $ git rm [file1] [file2] ...

       # Stop tracking the specified file, but the file will be remained in the Workspace.
       $ git rm --cached [file]

       # Rename the file and put the renamed name into the Index.
       $ git mv [file-original] [file-renamed]


5. ### Code Submission

       # Submit the code from the Index to the Repository.
       $ git commit -m [message]

       # Submit the specified file from the Index to the Repository.
       $ git commit [file1] [file2] ... -m [message]

       # Submit the changes in the Workspace since the last commit, to the Repository directly.
       $ git commit -a

       # Display all diff information when submitting.
       $ git commit -v

       # Use a new commit to take the place of the last commit.
       # If the code doesn't have any new changes, it will be used to rewrite the commit information of the last commit.
       $ git commit --amend -m [message]

       # Redo the last commit, including the new changes to the specified file.
       $ git commit --amend [file1] [file2] ...

6. ### Branch

       # List all local branches.
       $ git branch

       # List all remote branches.
       $ git branch -r

       # List all local branches and remote branches.
       $ git branch -a

       # Create a new branch, but still stay in the current branch.
       $ git branch [branch-name]

       # Create a new branch and switch to the branch.
       $ git checkout -b [branch]

       # Create a new branch, pointing to the specified commit.
       $ git branch [branch] [commit]

       # Create a new branch to establish a tracking relationship with the specified remote branch.
       $ git branch --track [branch] [remote-branch]

       # Switch to the specified branch and update the workspace.
       $ git checkout [branch-name]

       # Switch to the previous branch.
       $ git checkout -

       # Establish a tracking relationship between the existing branch and the specified remote branch
       $ git branch --set-upstream [branch] [remote-branch]

       # merge the specified branch to the current branch.
       $ git merge [branch]

       # Select a commit to be merged into the current branch.
       $ git cherry-pick [commit]

       # Delete the branch.
       $ git branch -d [branch-name]

       # Delete the remote branch.
       $ git push origin --delete [branch-name]
       $ git branch -dr [remote/branch]


9. ### References

    I have followed many articles but among them, the following articles are really helpful. Those articles helped me a lot and also encourage me to write this article according to my understanding.
 
     * [tutorialspoint](https://www.tutorialspoint.com/sdlc/index.htm)
     * [Top 12 SDLC Methodologies with Pros and Cons](https://www.techuz.com/blog/top-12-sdlc-methodologies-with-pros-and-cons/)
     * [SDLC Methodologies](https://svitla.com/blog/sdlc-methodologies)
     * [Top 6 SDLC Methodologies And How To Choose The Best One?](https://www.goodcore.co.uk/blog/sdlc-methodologies/)
     * [Top 7 SDLC Methodologies](https://hackr.io/blog/sdlc-methodologies)
     * [SDLC Models Explained: Agile, Waterfall, V-Shaped, Iterative, Spiral](https://existek.com/blog/sdlc-models/)
     * [TOP SOFTWARE DEVELOPMENT MODELS: THEIR PROS & CONS](https://cybercraftinc.com/blog/top-software-development-models-their-pros-cons)
     * [SDLC (Software Development Life Cycle) Phases, Methodologies, Process, And Models](https://www.softwaretestinghelp.com/software-development-life-cycle-sdlc/)
    * [Waterfall vs. Incremental vs. Spiral vs. Rad Model: Key Difference](https://www.guru99.com/compare-waterfall-vs-incremental-vs-spiral-vs-rad.html)
    * [What are the Different Types of Agile Methodologies?](https://www.wrike.com/project-management-guide/faq/what-are-the-different-types-of-agile-methodologies/)
    * [Agile Methodologies](https://www.blueprintsys.com/agile-development-101/agile-methodologies)
    * [Difference between V-model and Waterfall model](https://www.geeksforgeeks.org/difference-between-v-model-and-waterfall-model/)
    * [Choosing the right Software development life cycle model](https://melsatar.blog/2012/03/21/choosing-the-right-software-development-life-cycle-model/?fbclid=IwAR1mpCDGUxD0CuhdSWtgtHsUEXQWMtPi4aWCdG03P1p-bYoXXY9M_geNZl4)
    * [Spiral Model – What Is SDLC Spiral Model?](https://www.softwaretestinghelp.com/spiral-model-what-is-sdlc-spiral-model/)

    **[⬆ Back to Top](#table-of-contents)**

