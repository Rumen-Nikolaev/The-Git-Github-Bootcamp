# Branches

## Branches are an essential part of Git! Think of branches as alternative timelines for a project. 

- They let us create separate contexts to try new ideas or work on multiple features in parallel.

- Changes made on one branch do not affect other branches unless we merge those changes.

## The Master Branch

- The master branch: In Git, you are always working on a branch, and by default, this branch is named master.

- The master branch doesn’t have any special features or powers; it functions just like any other branch.

## Head

- We will often come across the term HEAD in Git. HEAD is simply a pointer that refers to the current location in your repository.

- It points to a particular branch reference. So far, HEAD always points to the latest commit you made on the master branch, but soon we will see that we can move around, and HEAD will change accordingly!

## Viewing Branches

```sh
   git branch
   ```

- Use git branch to view your existing branches. The default branch in every Git repository is master, though this can be configured to a different name if desired.

## Creating Branches

   ```sh
   git branch <branch-name>
   ```

- Use git branch <branch-name> to create a new branch based on the current HEAD. This command only creates the branch; it does not switch you to the new branch, so the HEAD remains the same.

## Way of switching

   ```sh
   git checkout <branch-name>
   ```
- Historically, we used git checkout <branch-name> to switch branches.
  
- This still works. However, since the checkout command performs many other functions, a standalone switch command was introduced to simplify branch switching.

## Creating and Switching

   ```sh
   git switch -c <branch-name>
   ```
- Use git switch -c flog to create a new branch and switch to it all in one go. The -c stands for "create".
