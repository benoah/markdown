# Git and Git Commands

### git init

The “git init” command will create a new git repository. It can also be used to initialize an existing repository. This command will create a sub directory in your folder called .git. This file contains all the meta data that you will need to interact with GitHub.
Create a folder on your desktop name it git_repo
CD into this folder using your terminal
When you are inside the folder type the following command: “git init”

You should get a message back that says git was initialized just as above.
Once you are done with the initialization, if you browse to the folder that you have just initialized git in, you should see a new folder .git.

- The “git init” command will create a new git repository. It can also be used to initialize an existing repository. This command will create a sub directory in your folder called .git. This file contains all the meta data that you will need to interact with GitHub.

- Create a folder on your desktop name it git_repo
- CD into this folder using your terminal
- When you are inside the folder type the following command: “git init”

### git status

Inside your git_repo folder, create a new test.txt file. It can be empty. This brings us to the “git status” command.
The “git status” command does the following: it displays the state of the directory that you are working in, also known as your working copy and it will display the staging area. The git staging area is a process just before you commit code to a GitHub repository. You can do final checks on code that you have written here.

- If you created a new test.txt file inside your git_repo folder and run “git status” in your terminal, you should get the following output:

**“On branch master” tells us what branch we are on. We will learn about branches later in this course.**
**“No Commits yet” confirms that no commits were made to this branch.**
**“Untracked Files” shows you a list of files that are untracked - this means that you have not committed it to staging yet.**

### Adding files to git

- You need to commit the files to a staging area. The staging area is the step just before you commit any files. In staging, you are still able to edit files. Git forces you to make sure that you are 100% sure about what you want to commit.

- Another great part about the staging area is that you can commit only files which are needed. For instance, if you are working on two features or sections of a website, the one being a gallery slider and the other being card for a website. Let’s say the gallery is done but the cards aren’t. You can stage the files for the gallery only and commit them as we will learn in the next lesson.

- For you to stage files that you want to add to a commit, you will need to use “git add test.txt” command. Since we only have a single file, we can use the command above to add that specific file. If we wanted to add all our files to staging, we could use the “git add" command. To view which files we have staged, we can use “git ls-files”.

### git commit

- Using the "git add" command is the first step in the process to adding our files to a GitHub repository. This will not be of much use to us if those files weren’t in a repository which is safe somewhere.
- Remember you need to be in the folder where all your source code is. CD into the repository that we created.
  For the second part of the process we will use the "git commit" command.

- “git” tells the command line that we are going to a command that git provides for us.
- “commit” tells git that we are now ready to commit some source files from our staging environment.
- “-m” tells git that we are going to add a message to our commit.

- “test 2344 This is a test file for Noroff Learners” gives an explanation about the commit. Remember when committing source code, be sure to say exactly what the code does. A good rule of thumb is to use the name of the website, the ticket number that you are working from JIRA, and a comment about the code.

- We must now connect to the repository that we created during the introduction of this course:
- "git remote add origin" https://github.com/norofftutor/noroffGITHUB.git
- “git” tells the command line that we are making use of a git command.
- “remote” tells git that we are connecting to a repository that is on their servers.
- “add” tells the git that we are going to add files to this remote repository.
- “origin” followed by the URL https://github.com/norofftutor/noroffGITHUB.git tells git which repository to add the files to. Please note that your URL will be different to mine as you have created a different repository to mine.

### Once you have connected to the repository you would need to run the following command:

- “git push -u origin master”

### If you execute the command above, you will get the above response from git. You might have to wait a while because your local machine is sending your source code files to a server.

- “push” tells git that it needs to push files from your local machine to git’s server.
- “-u” tells git that you are about to push upstream to its repository.
- “origin” is the URL that we set in the previous command.
- “master” is the name of the branch that we will commit.

**During this process you will need to login to git. Congratulations! You have just made your first git commit.**

### Feature Branching

- As you develop a web application as a team, epics will be broken down into user stories as you learnt with Agile in the previous lessons.

- You will be assigned a user story that you would need to complete. In that way, a huge task is broken down into smaller tasks and different developers will be working on different features. You would need to isolate your code somehow, and this is where feature branching or branching becomes useful.
  Master is always the main branch in git unless otherwise stated by your Scrum master. Therefore, it always needs to be in a working condition and ready to be pushed to a live website.

- This is how we will translate what we would like to do in a git command:

#### The command “git checkout -b noroffGalleryFeature” does the following:

> “checkout” tells git that you want to check out the latest code on master. A point to remember is that once you checkout the master branch, whatever code that is in master at that point will be available in your branch. If another developer checks code into master, your branch will not automatically update. It is up to you as the developer to merge the latest version of master into your branch.

- “-b” creates a new branch from master
- “noroffGalleryFeature” is the name of your new branch.

To test and see if that worked, you can use the following command:

- The command “git branch” will show you a list of branches that are available for your repository and the branch that you are on should have an asterisk next to it.
