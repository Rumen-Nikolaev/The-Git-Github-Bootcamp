# Github Basics Exercise

### 1. Create a new repository locally on your machine.
### 2. Create a new Github repository. Name it whatever you want.
  
   ```sh
   mkdir my-new-repo
   cd my-new-repo
   git init
   ```

### 3. Connect your local repo to the Github repo.
  
   ```sh
   git remote add origin https://github.com/your-username/my-new-repo.git
   ```

### 4. Optional: rename the default branch from master to main. 

   ```sh
   git branch -M main
   ```

### 5. Make a new file called favorites.txt  Leave it empty. Make your first commit on the main branch.

   ```sh
   touch favourites.txt
   git add favourites.txt
   git commit -m "Add empty favourites.txt file."
   ```

### 6. Push up your main branch to Github! Make sure you see your empty favorites.txt file on Github.

   ```sh
   git push -u origin main
   ```

### 7. Next, create two branches: foods and movies

   ```sh
   git branch foods
   git branch movies
   ```

### 8. Switch to the foods branch.  Add three (or more) of your favorite foods to the favorites.txt file.  Add and commit your changes on the foods branch.

   ```sh
   git checkout foods
   echo "Pizza\nSushi\nIce Cream" >> favorites.txt
   git add favourites.txt
   git commit -m "Add favourite foods"
   ```

### 9. Switch to the foods branch.  Add three (or more) of your favorite foods to the favorites.txt file.  Add and commit your changes on the foods branch.

   ```sh
   git checkout movies
   echo "Inception\nThe Matrix\nInterstellar" >> favorites.txt
   git add favourites.txt
   git commit -m "Add favourite movies"
   ```

### 10. Push up your foods branch to Github. Make sure you see it on Github!

   ```sh
   git push -u origin foods
   ```

### 11. Push up your movies branch to Github.  Make sure you see it on Github!

   ```sh
   git push -u origin movies
   ```

### 12. Merge the foods branch into the main branch.  Then merge the movies branch into the main branch.  If necessary, resolve conflicts so that you end up with your favorite foods and favorite movies in the same favorites.txt file. 

   ```sh
   git checkout main
   git marge foods
   git merge movies
   git add favorites.txt
   git commit -m "Resolve merge conflicts and combine favorites"
   ```

### 13. Push up the latest work on your main branch to Github.

   ```sh
   git push origin main
   ```

