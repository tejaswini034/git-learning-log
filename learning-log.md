# My Learning Log

## About This Project
I'm learning Git and version control *properly* to track my work.

## Goals
- [x] Understand how commits work
- [x] Understand the various Git commands
- [x] Learn branching and merging
- [x] Push my work to GitHub

## Points 
- Git is like a time machine for your files
- Every commit is a snapshot you can go back to
- Branches allow you to experiment without affecting the main project
- You can merge branches back together when ready

## The Process 
- git init
- git add
git add file_name
- git commit
git commit -m "message"
- git status
- git log **(Use `git log --oneline` for a compact version of your commit history)**  
---
- git checkout -b branch_name   (Alternatively, you can use the modern command: `git switch -c branch_name`) 
(creates a new branch with the branch name)
(If the branch exists, switch to it using: `git checkout branch_name`)
- git branch
- git merge
git merge other_branch
- git merge --abort   (to well abort the merging if a conflict arose and you want to pause and look back)  
---
- git push
- git pull
- git fetch (fetch a branch from github)
- git clone  
---
- git branch -d branch_name (delete branch locally)
- git branch -D branch_name (forced deletion if branch not fully merged)
- git push origin --delete branch_name (delete remotely if branch to be deleted from github too)   

## The setup (local repo to GitHub)
**If setting up for the first time**
- echo "# git-learning-log" >> README.md
- git init
- git add README.md
- git commit -m "first commit"
- git remote add origin https://github.com/your GitHub username/git-learning-log.git
(It assigns this URL the nickname origin (which is the industry standard name for your main remote server))
- git branch -M main
(Renames the current local branch to main (using the -M flag to force the rename))
- git push -u origin main (later you can just write git push)
- git push origin branch_name(if_exists)


**or push an existing repo**
- git remote add origin https://github.com/your GitHub username/git-learning-log.git
- git branch -M main
- git push -u origin main  

## What's origin?
It acts as a shortcut: Typing out a long URL like https://github.com/tejaswini034/git-learning-log.git every single time you want to push would be exhausting. By running git remote add origin <URL>, you are telling Git: "From now on, whenever I say 'origin', I mean this exact URL."  
So when you run git push origin main, you are telling Git: "Push my local 'main' branch to the remote destination nicknamed 'origin'."  
(I could use absolutely any other word other than origin - but that's the industry standard)

## graph symbols meaning 
- `*` means a commit
- | means history continuing 
- / or \ means a branch split or merge

## md files formatting
- `*ab*` for *italics*
- `**abc**` for **bold**
- `***abc***` for ***both***
- (backtick)...(backtick) to `highlight` code and commands
- Use triple backticks (```) on separate lines to highlight multi-line commands. 
- > To highlight a key takeaway, a warning, or a tip, use the greater-than symbol (>) to create a blockquote
---
- `---` (as used above) for dividers
- [`x`] as checkboxes
- `-` or `*` for bullets i.e - or *
- use double space for continuing on the next line

## Profile README
- A special repository that displays its README.md directly on your profile page.
- The repo name is the same as your username