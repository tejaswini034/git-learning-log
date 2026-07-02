<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Learn Git Fundamentals

**Project Link:** [View Project](https://nextwork.ai/projects/8bf3bcb5-a70d-418a-9c76-251365f69028)

**Author:** Tejaswini Ponnada  
**Email:** tejaswiniponnada06@gmail.com

---

![Image](https://nextwork.ai/determined_maroon_jolly_tamarind/uploads/8bf3bcb5-a70d-418a-9c76-251365f69028_l5jsusg6)

## Project Overview: Learning Git Version Control

### Goals and objectives

In this project, I'm building a GitHub repo to learn the git essentials of creating a repo, a branch, and handling merge conflicts.

## Setting Up the Development Environment

### Installing Git and Cursor

In this step, I'm verifying that I have git and it's working, my code editor is functioning, and I have a GitHub account. If not, I'll be installing git, setting up my preferred code editor and/or making that GitHub account. 

![Image](https://nextwork.ai/determined_maroon_jolly_tamarind/uploads/8bf3bcb5-a70d-418a-9c76-251365f69028_ryyzlsf8)

## Configuring Git and Creating the Learning Log

### Setting up Git identity and project file

In this step, I'm setting up Git to track changes across my local repo.

![Image](https://nextwork.ai/determined_maroon_jolly_tamarind/uploads/8bf3bcb5-a70d-418a-9c76-251365f69028_d6lm2bxt)

### Understanding global Git configuration

The --global flag means my configurations are applied by default to every single repository on my system. 
So using --global I only need to configure my name and email once, and that will be automatically applied to a newly created repo, rather than manually having to configure my details every time I create a new repo. 
I used a specific email because that's the email linked to my GitHub account, thus other users (and future me) can see that it was I who made changes to the repo and at what moment.

## Initializing a Repository and Making Commits

### Creating the first commits

In this step, I'm setting up a Git repo in the folder already created so that I can manage changes across my repo and commit said changes to GitHub. I'll also verify the commit history. 

![Image](https://nextwork.ai/determined_maroon_jolly_tamarind/uploads/8bf3bcb5-a70d-418a-9c76-251365f69028_blkivqea)

### Understanding git add vs git commit

git add prepares and stages the changes made to the file i.e it gathers the modified files into the staging area (like choosing which items to pack into a box and then putting them in the box - note that while the box is open i.e the file is only staged, any changes will not be permanently documented), while git commit saves a permanent snapshot with the existing file (like sealing the box and labelling it)

## Branching and Working in Parallel

### Creating and switching branches

In this step, I'm creating a merge conflict first creating a branch and then making two separate commits on the new branch and main so that I can figure out how to manage a merge conflict situation - via manual intervention 

![Image](https://nextwork.ai/determined_maroon_jolly_tamarind/uploads/8bf3bcb5-a70d-418a-9c76-251365f69028_drz4zcda)

### Why merge conflicts occur

A merge conflict happens because the same line(s) has/have two different data - how is Git supposed to decide on which context to keep and which to delete?

See Git is smart.  If you edit the top of a file on one branch, and edit the bottom of the same file on another branch, Git will easily merge them automatically because the changes do not overlap.

But when changes DO overlap i.e when you edit the exact same lines in different ways on two different branches, you create two competing versions of history.

A merge conflict happens because Git refuses to risk overwriting your valuable work by making a blind guess. It halts so that you can safely choose which changes to keep.

## Merging Branches and Resolving Conflicts

### Merging feature branches into main

In this step, I'm merging the main branch with the new branch created so that I can trigger a merge conflict - and then figure out how to solve it.

![Image](https://nextwork.ai/determined_maroon_jolly_tamarind/uploads/8bf3bcb5-a70d-418a-9c76-251365f69028_0e34g9cu)

### Interpreting Git conflict markers

The conflict markers show me the current branch and the incoming branch. 
The HEAD section contains the current branch I am on. The other section contains the branch I am merging from.
The ======= (equals signs) act as the divider line separating the two competing versions.

## Publishing to GitHub

### Creating a remote repository

In this step, I'm setting up the local repo on GitHub so that I can make it public (or document it in GitHub and just keep it private).

![Image](https://nextwork.ai/determined_maroon_jolly_tamarind/uploads/8bf3bcb5-a70d-418a-9c76-251365f69028_l5jsusg6)

### Pushing local commits to GitHub

I ran git push to push my local repository changes to the remote repository on GitHub. I needed to set up a remote first because Git needs to know the exact destination URL of where to upload our code. Without configuring a remote (which we usually nickname 'origin'), Git has no target address to send our local commit history to.

## Bonus: Building a GitHub Profile README

![Image](https://nextwork.ai/determined_maroon_jolly_tamarind/uploads/8bf3bcb5-a70d-418a-9c76-251365f69028_5y2qcn3e)

### Commands used to publish the Profile README

In this project extension, I used the commands git clone, git add, git commit, and git push to push my README to my repo on GitHub

## Reflections and Key Takeaways

### Tools and concepts mastered

The key tools I used include VSCode, Git, GitHub, and learn.nextwork.org.

### Time and challenges

This project took me approximately 8 hours. The most challenging part was understanding git merge.

### Looking ahead

I did this project today to learn how to use Git and work on GitHub. 

---

*Built with [NextWork](https://nextwork.ai) - [View this project](https://nextwork.ai/projects/8bf3bcb5-a70d-418a-9c76-251365f69028)*
