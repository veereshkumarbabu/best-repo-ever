Checkout to the branch that has a conflict: git checkout new-branch-2
Make sure your local repository is up to date: git pull
Merge master into the feature branch: git merge origin/master Notice you are merging the remote tracking branch and not your local copy of master—this is because the pull command updated the remote branches and the one you are on, but did not update master.

Crafting atomic commits is an important part of creating a readable and informative history of the project.

In a perfect world, you would never need to look at or change anything in your history. However, we don’t live in a perfect world, so version control lets us look into our change history if necessary. Each commit should be a small, logical unit of change and tell the story of your repository.

When you see there’s a conflict, that’s OK! Type git status to verify which file has the conflict. The files that have conflicts are listed under Unmerged Paths.
Open that file in your text editor, and look for the merge conflict markers. (<<<<<<<, =======, >>>>>>>)
Both branches’ versions of code are present—pick which code you want to keep and delete the other. Be sure to delete the merge conflict markers created by Git and save your changes.
Add and commit the saved changes to resolve the merge conflict:
Enter command: git add README.md
Enter command: git commit -m “Commit to resolve merge conflict”
Push the feature branch up to the remote: git push
