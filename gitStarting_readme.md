*Learning Git*

__________________________________________________________________________________
"""Using "*" to show headings and stuff because there's no bold and underlines
	#######################################################
I mean, I could just copy and paste in that format, but you know...."""
__________________________________________________________________________________


First task I got given at this new internship was to learn git, and seeing as I never knew it, I am sure that there are many other people who never used git before as well, so I will put my study journey in here. I asked ChatGPT steps to learning git. So here is me learning git by following the steps and sharing my journey with you hoping it helps as well.

________________________________________________________________________________

**Step 1: Understand the basics of version control**

"""
I personally agree with learning at least the fundamentals before doing something and then once you know that, go for a 'learning on the job' approach, so let's go through understanding the fundamentals and 'lingo'
"""

What is version control?

Basically, it is a system that tracks changes to files over time. It allows you to record changes, revert to previous versions and collaborate with other people without overwriting another persons work. Its purpose is to ensure that every change is documented as well as easily manage different versions of your project. This makes it easier to track, review and merge changes.


Types of Version control systems?

Local version control: Simplest form. Changes are tracked to your local machine. This isn't suitable for collaboration and is prone to error.

Centralized version control: All versions are stored in a central server. Users check files to make changes. This relies on a single server, and you lose everything if the server fails.

Distributed version control: Each user has a copy of the entire project history on their local machine, making it highly resilient and ideal for collaboration.



Now....why would we use git?

- Git allows multiple people to work on different parts of a project simultaneously through what is known as branches. Branches can be merged back in to the main code, this allows parallel development to take place.

- Every developer has a copy of the repository.

- Git maintains a history of changes, so you can easily revert to earlier versions if needed 

- git is designed to be highly efficient, even for larger projects 



Important words to know:
- Repository: This is where git stores all of its files, folders and history of changes. Can be local or remote 
- Commit: A commit is like a snapshot of your project at a certain point in time. records changes made to your files and serves as a versioning checkpoint 
- staging area: Before committing changes, you add them to the staging area. This area allows you to prepare changes that you want to include in your next commit 
- Branch: A branch is a separate line of development within a repository. By default, every repository starts with a branch called main or master. You can create new branches to work on features or fixes without affecting the main code.
- Merge: Merging is combining phases from different branches in to one.
- Clone: Duplicating a remote repository on your local machine. This allows you to work on it offline.
- Pull: The 'git pull' command fetches and integrates changes from a local repository into your main branch.
- Push: 'git push' command uploads your local commits to a remote repository, making your changes available to others.

"""
See why it is important to know the fundamental stuff before actually diving in?
Personally, just from learning these definitions I feel like I can use git with a little more confidence.

There's still more to learn here, so let's dive a little more deeper.
"""

Git workflow:

1. Initialize a repository: Start a new repository with 'git init' or clone one using 'git clone'
2. Make changes: Edit files and make improvements
3. Stage changes: Use 'git add <file>' to move your changes to the staging area
4. Commit changes: Use 'git commit -m "message"' to save changes to repo
5. Push changes: If working with a remote repo, push commits using 'git push'


Difference between GitHub and git:
Git: Open-source vcs that you install on your machine. Tracks changes to files and helps manage project history.
GitHub: A cloud-based platform that hosts git repositories, making it easier to share and collaborate with others. Has features like pull requests, issue tracking, and project management 


Some resources if you feel that you would like to know more:

Git documentation: [link](https://git-scm.com/doc)
Pro Git Book: [link](https://git-scm.com/book/en/v2)
GitHub guides: [link](https://docs.github.com/en)


_______________________________________________________________________________________________

**Step 2: Install git and set-up GitHub**

Obviously the most important part of using something is installing it. Like, how else would you utilize it?


So...... Installing Git.... 

Installing on Windows:
    - Go to the website: [link](https://git-scm.com)
    - Download latest version of git
    - Open the installer and follow the instructions wizard
        - You'll be prompted to choose a text editor. Default is Vim, but you can change it 
        - If you're a beginner (Why you reading this if you're not? lol), it would be best to choose "Use git from Git Bash only"
        - Leave the rest as default 
    - Once installed, open Git Bash 

MacOS:
    - Open the terminal 
    - Install Git using homebrew
        - brew install git
        - Alternatively ~ Go to the website: [link](https://git-scm.com)
    - Check version
        - git --version

Linux:
    - Open the terminal
    - Use package manager to install git 
        - sudo apt update
        - sudo apt install git 
    - Check version after installation
        - git --version


Configuring Git

Honestly, the simplest part 

Set up your name:
    - git config --global user.name "Your name"

Set up your e-mail:
    - git config --global user.email "e-mail"

And like that, git is configured


If you don't wanna constantly enter your user name and password each time you use GitHub when authenticating push/pull changes, you can set up SSH keys, but since it is optional, I'm not gonna include it in here.


Then create a GitHub account..
If you've created any type of account online, you should know how to do this. I'm not going to hold your hand and tell you to enter your e-mail in the designated e-mail part, and definetly not tell you to enter your password in the password area. And then after that, when it asks your preference, just skip that, because entering something wrong there can affect your visibility, then you'll be in. Like, how helpless are you, hmph!!! 


Now that you have both set up, it is time to connect git to GitHub

Here is the https method:
    -Create a repository:
        - Go to GitHub profile
        - repository -> New
        - Give repository a name and select public or private 
        - Click on "Create Repository"
    - Connect local repository 
        - it remote add origin https://github.com/username/repository.git
    - push changes
        - When pushing for the first time:
            - git push -u origin main


Verify your set-up
    - clone repository from GitHub
        - git clone https://github.com/username/repository.git
    - Make a change
        - git add <filename>
        -git commit -m "Initial Commit"
    - push the change 
        - git push


Fun things to do in GitHub:
<We Getting crazy with these ones lol>
    - Create repositories
        - public and private repos for your projects 
    - Fork repositories
        - Make your own copies of someone elses repositories
    - Issues 
        <Warned you that we'd be getting crazy>
        - Track bugs and features for projects
    - Pull requests 
        - Contribute to other projects or collaborate on your own


____________________________________________________________________________________________________


**Step 3: Learn Basic Git commands**


***Initialize a new git repository*** 

To start tracking your project with git, you need to initialize a git repository. This creates a hidden .git folder

command:
    - git init

example:
    - mkdir my-project 
    - cd my-project 
    - git init



***Clone an existing repository***

If you want to work on a project that already exists in GitHub, you need to clone it to your local machine 

Command:
    - git clone <repository url>



***Check status of your files***

It is important to check the status of your files once you start making changes to your projects 
This command tells you which files have been modified

Command:
    - git status



***Add changes to staging file***

Before committing changes, you need to send them to the staging area

Command:
    - git add <filename>



***Commit Changes***

Once changes or staged, you'll need to commit them

command:
    - git commit -m "commit message"


***View command history***

Can view the history of all commits made in a repo, including commit messages, author and timestamps

command:
    - git log



***Push changes to a remote repo***

If you have a remote repo, like on GitHub, ou need to push your commits to that repo so that people can actually see your changes 

command:
    - git push origin <branch name>

[git push origin main] -> Pushes the changes from your local repository to the "main" branch of the remote repo



***Pull changes from a remote repo***

If someone else made a change to a remote repo, you can pull those changes to update your local repo

command:
    - git pull origin <branch-name>



***Create a new branch***

Branches allow you to work on seperate features, bug fixes or experiments without affecting the main codebase

Command:
    - git branch <branch-name>



***Switch between branches***

After creating a branch, you can switch to it to start working on it  

Command:
    - git checkout <branch-name>



***Merge branches***

Once you're done with a branch, you can merge it back in to the main branch or any other branch 

Command:
    - git merge <branch-name>



***Discard unchanged changes***

If you've made any changes that you don't want to keep, you can just discard them

Command:
    - git checkout -- <filename>



***Remove files from staging area***

If you've staged a file you'd no longer like to commit, you can remove it from the stagihng area without deleting the file


Command:
    - git reset <filename>


From what I can tell, these are the main ones required to manage everyday tasks in git.


____________________________________________________________________________________________


**Step 4: Understanding Branching and merging**

Branching and merging are two of the most powerful features of git..... apparently. They allow you to work on different features, bug fixes or experiments without affecting the main codebase. This will also help give a actual reasons why you'd need the above stuff.


Let's start with the basics.... What is a branch?

A branch in git represents an independant line of development. Like creating a new timeline that has no effect on the main project
    - This allows you to:
        - Work on new features without disturbing the main branch
        - Collaborate on the mainbase without conflicting with other peoples work
        - Safely experiment with new ideas and roll back if necessary

each git repository starts with a default branch called "main"


Now I would tell you the command as we go, but if you don't know what code I'm explaining, it means you skipped over that part, and I do not reward bad behaviour....gave that list for a reason.......

To add an additional branch to work outside of main, the above command to add a branch will do that. 

Now that you understand why having multiple branches helps a lot with production, you should probably also switch between each branch, right? 
The code to do that is above as well ;)


Seriously now, we'll go in to branch specific features I never cover yet:

***View all branches***

Self-explainatory
    - git branch


***Delete a branch***

Again, self explainatory:
    - git branch -d <branch name>




Make changes on a branch:
    - Modify files 
    - Stage changes
    - Commit changes


______________________________________________________________________________________________

**Step 5: Learning to use git for remote repos**

Before pushing your local git project to a GitHub, you'll need to create a repository 

Steps:
    - Log in to GitHub account 
    - Click the '+' icon in the top-right corner and select new repository
    - Enter a name for your repository 
    - Can add a description if you'd like
    - add a readme to your repo
    - Click on create repository

Once you create your repository, GitHub will give you instructions or pushing or cloning your existing repository to your local machine



***Add a remote repository to your local project***

If you have an existing local git that want to link it to 

Command:
    - git remote add origin <repository url>



***Push local changes to GitHub***

Once you've added the remote repository, you can push your local changes to GitHub

command:
    - git push -u origin <branch name>

The "-u" makes it so that future pushes only require "git push"



***Clone a repository from GitHub***

Cloning is the process of downloading a repository from GitHub to your local machine

Command:
    - git clone <repository url>



***Pull changes from GitHub***

If other collaborators have pushed changes to the remote repository, you'll want to pull those changes to update your local repo

command:
    - git pull origin <branch name>



***Fork a repository on GitHub***

This is a feature that allows you to copy someone elses repo to your GitHub account

Steps: 
    - Navigate to the repository that you want to fork
    - Click the fork button on the upper-right corner of the repo
    - A copy will be added to your GitHub account



***Create a pull request***

A pull request is a way of proposing changes to a repo. If you're working in a branch or a fork, you can create a pull request to request that your changes be reviewed and merged into the original project.

Steps to create a pull request:
    - Push your branch with the changes to GitHub
    - Navigate to the original repo
    - Click on the pull requests tab
    - click "new pull request"
    - Select the branch that you want to mrge from
    - Review the changes 

Thats about all that seemed important, we'll just go over pull requests quick, then you should be sorted

____________________________________________________________________________________________________


**Step 6: Work with pull requests**

In collaborative projects, PRs are an important feature for managing contributions and ensuring quality control. They allow developers to propose changes and have them reviewed by others


Cool......What exactly is a pull request tho?

It is a way for devs to notify others about changes they've made to a repo. When opening a request, you're requesting that the changes from your branch be merged in to another branch

Purpose:
    - Review code before merging it 
    - Allow discussion and collaboration on changes 
    - Ensure code quality by getting teammates 
    - Catch issues or conflict before integrating the code 



***Creating a pull request***

Once you've made changes in a branch and pushed these changes to a remote repo, you can create a pull request 

Steps to create a pull request:
    - Push your branch with the changes to GitHub
    - Navigate to the original repo
    - Click on the pull requests tab
    - click "new pull request"
    - Select the branch that you want to mrge from
    - Review the changes

(Just copied and pasted incase you missed it)

That is like it. You will inevitably run in to problems and stuff, but you learn best by fixing those, and I can't list every potential issue. I don't think that's possible at all 


Anyways, hope this helped you in someway to not find git or GitHub intimidating and I'll probably go over Obsidian next

______________________________________________________________________________________________________________________________
