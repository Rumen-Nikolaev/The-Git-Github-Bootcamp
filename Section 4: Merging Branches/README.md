# Merging

## Branching makes it super easy to work within self-contained contexts, but often we want to incorporate changes from one branch into another. We can do this using the git merge command.

- Switch to or checkout the branch you want to merge the changes into (the receiving branch).

- Then, use the git merge <branch-name> command to merge changes from the specified branch into the current branch.

```sh
   git switch master
   git merge bugfix
   ```
