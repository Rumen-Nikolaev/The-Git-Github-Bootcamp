# Git Diff Exercise

### Part 1: Setup. Please run the following commands from your terminal. Make sure you are not inside of a Git repo.

- Change into the newly created folder called `git-diff-exercise`.  You will be on a branch called `current` by default.
  
- Run `git switch 1970s`
  
- You should now have two branches that you can move between: `current` and `1970s` Each branch contains two files: `queen.txt` and `fleetwoodmac.txt`

#### Clone the repository:
   ```sh
   git clone https://github.com/Colt/git-diff-exercise
   ```

#### Change into the git-diff-exercise directory:
   ```sh
   cd git-diff-exercise
   ```

#### Switch to the 1970s branch:
   ```sh
   git switch 1970s
   ```

### Part 2: The Diffs

1. Compare the difference between the `1970s` branch and the `current` branch across all files

   ```sh
   git diff current..1970s
   ```
   
2. Compare the difference between the `1970s` branch and the `current` branch but only for the queen.txt file

   ```sh
   git diff current..1970s -- queen.txt
   ```
   
3. Switch over to the `current` branch if you are not currently on it.   Run a diff to compare the current HEAD to the previous commit (you could use the commit hash or reference HEAD's parent commit)

   ```sh
   git switch current
   ```
   
4. While on the `current` branch, change the `queen.txt` file by replacing Adam Lambert with your own name.  Save the change.  Add `queen.txt` to the staging area.  DO NOT COMMIT YET!

   ```sh
   git diff HEAD-1
   ```
   
5. Edit the `fleetwoodmac.txt` file, changing the lead singer from Stevie Nicks to Stevie Chicks (one of my chickens).  Save the file, but do not stage it.

   ```sh
   sed -i 's/Adam Lambert/Your Name/' queen.txt
   git add queen.txt
   sed -i 's/Stevie Nicks/Stevie Chicks/' fleetwoodmac.txt
   ```
   
6. Run a diff that would reveal the unstaged changes in the working directory (you should see only the change to `fleetwoodmac.txt` printed out)

   ```sh
   git diff
   ```
   
7. Run a diff that would reveal only the staged changes (you should only see the change to `queen.txt` printed out)

   ```sh
   git diff --cached
   ```
   
8. Run a diff that prints all changes (staged and unstaged) since the prior commit (you should see both changes printed out)

   ```sh
   git diff HEAD
   ```
