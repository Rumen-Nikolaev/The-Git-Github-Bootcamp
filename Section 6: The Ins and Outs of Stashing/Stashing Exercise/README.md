# Stashing Exercise

### Initialize a new git repo in a folder

   ```sh
   mkdir stashing_exercise
   cd stashing_exercise
   git init
   ```

### Create a file called diary.txt.  Inside the file, add the following: I love my boss

   ```sh
   echo "I love my boss" > diary.txt
   ```

### Add and commit the changes on the master branch

   ```sh
   git add diary.txt
   git commit -m "Initial commit with positive diary entry"
   ```

### Create a new branch called the-truth. Switch to it.

   ```sh
   git checkout -b the-truth
   ```

### In the diary.txt file, erase the contents and instead replace it with: I HATE MY BOSS
I HATE MY BOSS
I HATE MY BOSS
I HATE MY BOSS
I HATE MY BOSS

   ```sh
   echo -e "I HATE MY BOSS\nI HATE MY BOSS\nI HATE MY BOSS\nI HATE MY BOSS\nI HATE MY BOSS" > diary.txt
   ```

### OH NO! Your boss is walking towards you! Quick, switch over to the master branch!

   ```sh
   git checkout master
   ```

### WHATTT? The diary.txt file still contains our confession?  Quick, stash the changes before your boss sees!!

   ```sh
   git stash
   ```

### Your diary.txt file should now only contain "I love my boss"

   ```sh
   echo -e "I love my boss\nI love my boss\nI love my boss" >> diary.txt
   git add diary.txt
   git commit -m "Add more positive statements to diary"
   ```

### As your boss walks by, add more lies to the diary.txt file: I love my boss
I love my boss
I love my boss

   ```sh
   git checkout the-truth
   ```

### Add and commit your changes on the master branch.

   ```sh
   git stash pop
   ```

### Now that your boss has left, it's safe to get back to the truth! Switch over to the the-truth branch.

   ```sh
   git add diary.txt
   git commit -m "Restore the truth about boss in diary"
   ```








