# 1. Staging

The first step. References changes that are tracked, but are not implemented to repository just yet.

> Can use the command `git add -A` to add all the *unstaged* files.

# 2. Commiting

This step is a "checkpoint" for the repository. We can go back to each commit that we make in the repository if we find a bug or want to revert to an older version of the project.

> Use the command `git commit -m` to add a message with the commit.
> Also, can use the command `git commit -a` to skip **staging**.

# 3. Branches and Merging

We can create separate "backups" of our files, and work on different changes on each branch. 
After we have finished working on each change, we can then merge the branches with our `master` branch, so we can have those modifications in the main project.

> To merge two branches, use the command `git merge BRANCH`

# 4. Pulling and Pushing

After we have added a remote origin, we can add that origin to the Git repository, which allows us to push and pull changes to GitHub.

## Pulling
This command allows us to retrieve the latest changes that we have commited to the GitHub repository. It is a two-step process, in which we invoke the commands `fetch` and `merge` sequentially, to have the modifications in our current branch.

## Pushing
Is the inverse of pulling. Instead of retrieving changes FROM GitHub, we implement changes TO the origin (GitHub).
We just have to commit the changes, and pull the files that we have commited so far.

