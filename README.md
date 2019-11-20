# git-tutorial

# Simple Git Commands

## These are the steps for cloning a repository from github and modify it.
- Go to the folder you wish to clone the repository to and type `git clone <link from github>`. this will clone the remote repository from github to you machine.

- Whenever you decide to work on the project again, type `git pull` to pull cahnges made by others into your local repository.

- After making changes to your local repository type `git status` to see the files you modified
- Once you know the files you changed, type `git add <fileName>` to add the files to the list of files to commit.
- Once you add all the files, type `git commit -m "Description of changes made"` to apply these changes to your local repository.
- Once you commit all changes, type `git push` to apply these changes to the remote repository. Sometimes, when you try to push, git will warn you your branch is not up to date. This means there were changes made to the remote repository that you do not have in your local one. To fix that, type `git pull`, check for conflicts with the changes you made, then push again.

### Other useful commands
- `git reset <fileName>` The oposite of `git add`
- `git reset --soft HEAD~1` undoes the last `git commit`
- `git checkout <branchName>` switches branches
- `git checkout -b <branchName>` creates branch
- `git rebase <branchName>` merges branchName into your current branch. Be sure to `git pull` that branch before running this. There might be merge conflicts. Go to your editor and fix those conflicts manually then run `git rebase --continue`

### Good practices

- When working on new features, always create a branch with name `feature/featureName`
- When working on a big FIX, always create a branch with name `fix/fixName`. For minor bug fixes, make changes directly on `master`

    After you complete work on your branch, go into to github and make a `Pull Request`. 
    In there, describe your changes and select people to review them.
    Once your changes are reviewed and approved, they will be merged into the `master` branch
