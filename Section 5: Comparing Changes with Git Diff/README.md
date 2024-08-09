# Git Diff

## We can use the git diff command to view changes between commits, branches, files, our working directory, and more. We often use git diff alongside commands like git status and git log to get a better understanding of a repository and how it has changed over time.

   ```sh
   git diff
   ```

- Without additional options, git diff lists all the changes in our working directory that are not staged for the next commit.

## Diff-ing Specific Files

- We can view the changes within a specific file by providing git diff with a filename

   ```sh
   git diff HEAD [filename]
   ```

   ```sh
   git diff --staged [filename]
   ```

## Comparing Commits

- To compare two commits, provide git diff with the commit hashes of the commits you want to compare. For example: git diff <commit-hash1> <commit-hash2>.

   ```sh
   git diff commit1..commit2
   ```

- git diff HEAD lists all changes in the working tree since you last commit.

   ```sh
   git diff HEAD
   ```
- git diff --staged (or --cached) lists the changes between the staging area and the last commit.

   ```sh
   git diff --staged
   git diff --cached
   ```
