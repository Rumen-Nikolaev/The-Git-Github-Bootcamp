# Git Merging Exercise

## Part 1: Fast Forward Merge

### Your goal is to generate a fast forward merge. Demonstrate that you understand how FF merges work by creating one on your own! Make a new branch. Do some work in the repo such that when you merge the new branch into master, it results in a fast forward merge.  Merge that branch into master and see if you were right!

#### Create a new repository and add a file:
  ```sh
  mkdir fast_forward_demo
  cd fast_forward_demo
  git init
  touch greetings.txt
  echo "Hello" > greetings.txt
  git add greetings.txt
  git commit -m "Initial commit with greetings.txt" 
  ```


#### Create a new branch and make changes
   ```sh
   git checkout -b new_greetings
   echo "Hola" >> greetings.txt
   echo "Bonjour" >> greetings.txt
   git add greetings.txt
   git commit -m "Add greetings in Spanish and French"
   ```

#### Switch back to the master branch and merge the new branch:
   ```sh
   git checkout master
   git merge new_greetings
   ```

## Part 2: Merge Commit (No Conflicts)

### Your goal is to generate a merge commit with NO MERGE CONFLICTS. Create a new branch. Make some changes to the repo such that when you merge the new branch into master, it results in a merge commit.  The merge should not result in any conflicts. Merge that branch into master and see if you were right!

#### Create a new repository and add a file:
   ```sh
  git checkout -b new_greetings_v2
  echo "Ciao' >> greetings.txt
  echo "Hallo" >> greetings.txt
  git add greetings.txt
  git commit -m "Add greetings in Italian and German"
  ```

#### Create a new repository and add a file:
   ```sh
  git checout master
  echo "こんにちは" >> greetings.txt
  git add greetings.txt
  git commit -m "Add greeting in Japanese"
  ```

#### Merge the new_greetings_v2 branch into master:
   ```sh
  git merge new_greetings_v2
  ```

## Part 3: Conflicts!

### Your goal is to generate merge a conflict! Create a new branch. Make some changes to the repo such that when you merge the new branch into the master branch, it results in a merge conflict. Merge that branch into master and see if you were right! Resolve the conflict!

#### Create a new branch and make conflicting changes:
   ```sh
  git checkout -b conflicting_changes
  echo "Salut" >> greetings.txt
  git add greetings.txt
  git commit -m "Add a greeting in Romanian"
  ```

#### Switch back to the master branch and make conflicting changes:
   ```sh
  git checkout master
  echo "Salut" >> greetings.txt
  git add greetings.txt
  git commit -m "Add greeting in Romanian on master"
  ```

#### Merge the conflicting_changes branch into master:
   ```sh
  git merge conflicting_changes
  ```
