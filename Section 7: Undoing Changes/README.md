# Checkout

### The git checkout command is akin to a Swiss Army knife for Git, offering a wide range of functionalities.
 - Many developers find it overly versatile, which prompted the introduction of git switch and git restore for more specific tasks. With checkout, you can create and switch branches, restore files, and revert history.

- You can use git checkout <commit-hash> to view a previous commit. To find the commit hash, use the git log command. Typically, you only need the first 7 digits of the commit hash.

   ```sh
   git checkout d8194d6
   ```

- git checkout supports a somewhat unusual syntax for referencing previous commits relative to a specific commit. HEAD~1 refers to the commit before HEAD (the parent). HEAD~2 refers to the commit two steps before HEAD (the grandparent).

  ```sh
   git checkout HEAD~1
   ```

  ### Discarding Changes

  - If you've made changes to a file but want to discard them, you can revert the file to its last committed state using git checkout HEAD <filename>. This command discards any changes in that file, returning it to the version at HEAD.
 
   ```sh
   git checkout HEAD <file>
   ```

- Another Option: Here’s another, shorter option to revert a file: instead of typing HEAD, you can use -- followed by the file you want to restore. For example, git checkout -- <filename>.
 
    ```sh
    git checkout -- <file>
    ```

 ### Restore

- git restore is a brand new Git command designed to help with undoing operations.
- Since it’s so new, most existing Git tutorials and books don’t mention it, but it’s worth knowing!
- Recall that git checkout performs a multitude of different tasks, which many Git users find confusing.
- git restore was introduced alongside git switch as alternatives to some of the uses for checkout.

### Unmodifying Files with Restore

- If you've modified a file since your last commit and decide you don't want to keep those changes, you can revert the file to its last committed state using:

    ```sh
    git restore <file-name>
    ```
    
- git restore <file-name> uses HEAD as the default source to restore a file, but you can specify a different source with the --source option.
- For example, git restore --source HEAD~1 home.html will revert home.html to its state from the commit before HEAD.
- You can also use a specific commit hash as the source.

    ```sh
    git restore --source HEAD~1 app.js
    ```

- If you’ve accidentally added a file to the staging area with git add and want to exclude it from the next commit, you can remove it from staging using git restore.
- Use the --staged option like this:

    ```sh
    git restore --staged <file-name>
    ```

### Git Reset
- If you’ve made a few commits on the master branch but intended to make them on a different branch, you can undo those commits using git reset.
- Running git reset <commit-hash> will revert the repository to the specified commit, effectively removing the commits that followed.

    ```sh
    git reset <commit-hash>
    ```

### Git Reset
- If you’ve made a few commits on the master branch but intended to make them on a different branch, you can undo those commits using git reset.
- Running git reset <commit-hash> will revert the repository to the specified commit, effectively removing the commits that followed.

    ```sh
    git reset <commit-hash>
    ```

### Reset --hard
- If you want to undo both the commits and the changes made to your files, you can use the --hard option.
- For example, git reset --hard HEAD~1 will remove the last commit and discard the changes associated with it.

    ```sh
    git reset --hard <commit>
    ```

### Git Revert
- git revert is similar to git reset in that both are used to "undo" changes, but they work in different ways.
- While git reset moves the branch pointer backward and removes commits, git revert creates a new commit that undoes the changes introduced by a previous commit.
- Because it generates a new commit, you'll be prompted to enter a commit message.

    ```sh
    git revert <commit-hash>
    ```
