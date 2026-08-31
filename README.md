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
- git add (to stage)
git add file_name
- git rm --cached <file>..." (to unstage)
- git commit
git commit -m "message"
- git status
- git log **(Use `git log --oneline` for a compact version of your commit history - q to exit)**  
---
- git checkout -b branch_name   (Alternatively, you can use the modern command: `git switch -c branch_name`) 
(creates a new branch with the branch name)
(If the branch exists, switch to it using: `git checkout branch_name`)
(The convention of branch name is feature/<issue-number>-<description> - like feature/3-add-next-steps)
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

- git branch -D branch_name (forced deletion if branch not fully merged - usually after squash merge - Git creates a brand-new commit with different hashes. Your original branch commits don't appear in main's history anymore so -d thinks the branch isn't merged, even though the content is there.)

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

## Github to local repo 
- git pull origin main (first ensure you're on main by git checkout main)
(after a PR is merged, we still need to pull that to main)

## What's origin?
It acts as a shortcut: Typing out a long URL like https://github.com/tejaswini034/git-learning-log.git every single time you want to push would be exhausting. By running git remote add origin <URL>, you are telling Git: "From now on, whenever I say 'origin', I mean this exact URL."  
So when you run git push origin main, you are telling Git: "Push my local 'main' branch to the remote destination nicknamed 'origin'."  
(I could use absolutely any other word other than origin - but that's the industry standard)

# Issues
- Create an Issue on Github - assign it to yourself or someone else

# pushing a new branch to Github when that branch doesn't exist on Github yet
- git push --set-upstream origin <branch_name>
(The --set-upstream flag tells Git to create the branch on GitHub and link your local branch to it. This is only needed the first time you push a new branch. Future pushes on this branch only need git push because the link is already set.)

# Pull Requests
- Go to Pull Requests tab on Github. If you pushed a new branch to Github there should be a Compare & Pull Request option
- In the description body, type Closes #<issue_number> (like #1) - this will automatically close the issue 
- PR is now on Github - everyone gets the changes but it hasn't been merged into main yet
- Review the merge pull request on Github
- If all's fine, merge and cleanup by deleting the branch on Github
- On VSCode, git checkout main and git pull origin main

When you join a professional software team, your workflow will look like this combination of local Git and GitHub PRs:
1. Create a branch locally: You switch to a new feature branch (e.g., git checkout -b feature/add-login).
2. Do your work: You edit files, test them on your computer, stage, and commit.
3. Push your branch: You push your feature branch to GitHub (git push origin feature/add-login).
4. Open a PR: You go to GitHub, open a PR from feature/add-login to main.
5. The Conflict Stage: If a teammate edited the same file and merged their PR first, GitHub will warn you on your PR page: "This branch has conflicts that must be resolved."
6. The Resolution: You don't merge on GitHub yet. Instead, you run git pull origin main on your computer (while still on your feature branch) to bring their changes down, solve the conflict markers locally, commit the resolution, and push.
7. Merge: Once the conflicts are solved and your team reviews your code, you finally merge the PR on GitHub

Oh also 
- git branch -d feature/branch_name
(to delete the feature branch on your local machine)
(On Github just use the button)

- git branch -D feature/branch_name
(if you did a squash merge)
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
- `<!-- xyz -->` for comments in the md file (not visible)

## Profile README
- A special repository that displays its README.md directly on your profile page.
- The repo name is the same as your username

## Resources
- [Learn Git Fundamentals](https://learn.nextwork.org/projects/8bf3bcb5-a70d-418a-9c76-251365f69028) - Hands-on practice with Git basics
- [Collaborate with Pull Requests](https://learn.nextwork.org/projects/3ac00a14-cbfc-476a-9a2f-2d9b678880b9) - Hands-on practice with branches, PRs, and merge strategies
- [Pro Git Book](https://git-scm.com/book/en/v2) - Free comprehensive Git reference
- [GitHub Docs](https://docs.github.com) - Official GitHub documentation
- [Oh My Git!](https://ohmygit.org) - Interactive game to learn Git

# Meaning of Closes #4
When your PR description contains a keyword like Closes #1, GitHub automatically closes the linked Issue when the PR merges into the default branch. 


## Next Steps
- Learn about rebasing and interactive rebase
- Explore GitHub Actions for automation
- Practice contributing to open source projects

# Pull request template
- mkdir .github
- create a file - pull_request_template.md
- save, commit, push
For different templates: 
- .github/PULL_REQUEST_TEMPLATE/bug_fix.md
- .github/PULL_REQUEST_TEMPLATE/new_feature.md