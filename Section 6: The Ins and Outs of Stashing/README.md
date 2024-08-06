# Stashing

## Stashing allows Git to temporarily save uncommitted changes so you can come back to them later without making unnecessary commits.

## Git Stash

- The git stash command is a valuable tool for saving changes you're not ready to commit yet. It allows you to stash both staged and unstaged changes, effectively reverting your working directory to its last committed state.

- You can then return to these stashed changes later when you're ready.

```sh
   git stash
   ```

- Use git stash pop to remove the most recently stashed changes from your stash and apply them back to your working directory.

```sh
   git stash pop
   ```

### Stash Apply

- You can use git stash apply to apply the changes from your stash without removing them. This is useful if you want to apply the stashed changes to multiple branches.

 ```sh
   git stash apply
   ```

### Stashing Multiple Times

- You can add multiple stashes to the stack, with each new stash being added in the order you created them.

 ```sh
   git stash
   git stash
   git shash
   ```

### To apply a specific stash, you can use git stash apply stash@{n}, where n is the index of the stash you want to apply. By default, git stash apply applies the most recent stash.


 ```sh
   git stash apply stash@{2}
   ```

### Dropping Stashes

- To delete a particular stash, you can use git stash drop <stash-id>

 ```sh
   git stash drop stash@{2}
   ```

### Clearing the Stashes

- To clear out all stashes, run git stash clear

 ```sh
   git stash clear
   ```
