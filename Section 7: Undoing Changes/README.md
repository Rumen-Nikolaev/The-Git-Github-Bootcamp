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

  
