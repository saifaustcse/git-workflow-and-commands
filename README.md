# Find me

> If you think that these can be improved in anyway, please do suggest. Pull Request are highly appreciated. Find me if you wish [@Saif(https://www.linkedin.com/in/saif-aust-cse/).


1. ### Create a New Repository

       # Create a new Git repository in the current directory.
       $ git init
       
       # Create a new directory and initialize it to the Git repository.
       $ git init [project-name]
       
       # Download a project and its entire code history.
       $ git clone [url]


2. ### Configuration
    The setting file for Git is .gitconfig, which can be placed under the user's home directory (global configuration) or under the project directory (project configuration).

       # Display the current Git configuration.
       $ git config --list
      
       # Edit Git Configuration File.
       $ git config -e [--global]
       
       # Set the user information when submitting code.
       $ git config [--global] user.name "[name]"
       $ git config [--global] user.email "[email address]"

3. ### Add/Delete Files

       # Add the specified file to the Index.
       $ git add [file1] [file2] ...

       # Add the specified directory to the Index, including subdirectories.
       $ git add [dir]

       # Add all the files in the current directory to the Index.
       $ git add .

       # Being asked to confirm it before adding every change.
       # For multiple changes to the same file, split submission is supported.
       $ git add -p

       # Delete the files in the Workspace and put this deletion into the Index.
       $ git rm [file1] [file2] ...

       # Stop tracking the specified file, but the file will be remained in the Workspace.
       $ git rm --cached [file]

       # Rename the file and put the renamed name into the Index.
       $ git mv [file-original] [file-renamed]


2. Configuration
11. ### References

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

