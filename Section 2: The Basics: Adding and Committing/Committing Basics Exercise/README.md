1. Create a new folder called Shopping:

   ```sh
   mkdir Shoppoing
   ```

2. Initialize a new git repo inside of the Shopping folder (make sure you're not already inside of a Git repo!)

   ```sh
   cd Shopping
   git init
   ```

3. Make a new file called yard.txt

   ```sh
   touch yard.txt
   ```

4. Make another new file called groceries.txt

   ```sh
   touch groceries.txt
   ```

5. Make a commit that includes both empty files.  The message should be "create yard and groceries lists"
   
   ```sh
   git add yard.txt groceries.txt
   git commit -m "create yard and groceries lists"
   ```
   
6. In the yard.txt file, add the following changes:
- 2 bags of potting soil
- 1 bag of worm castings

   ```sh
   echo "- 2 bags of potting soil" >> yard.txt
   echo "- 1 bag of worm castings" >> yard.txt
   ```

7. In the groceries.txt file, add the following:
- 4 tomatoes
- 6 shallots
- 1 fennel bulb

   ```sh
   echo "- 4 tomatoes" >> groceries.txt
   echo "- 6 shallots" >> groceries.txt
   echo "- 1 fennel bulb" >> groceries.txt
   ```

8. Make a new commit, including ONLY the changes from the groceries.txt file.  The commit message should be "add ingredients for tomato soup"

   ```sh
   git add groceries.txt
   git commit -m "add ingrdients for tomato soup"
   ```

9. Make a second commit including ONLY the changes to the yard.txt file.  It should have the commit message "add items needed for garden box"

   ```sh
   git add yard.txt
   git commit -m "add items needed for garden box"
   ```

10. Next up, add the following line to the end of groceries.txt
- couple of seed potatos

   ```sh
   echo "- couple of seed potatoes" >> groceries.txt
   ```

11. In the yard.txt file, change the first line so that it says "3 bags of potting soil" instead of "2 bags of potting soil"
- 3 bags of potting soil
- 1 bag of worm castings

   ```sh
   sed -i 's/2 bags of potting soil/3 bags of potting soil/' yard.txt
   ```

12. Make a commit that includes the changes to BOTH files.  The message should read "add items needed to grow potatoes"

   ```sh
   git add yard.txt groceries.txt
   git commit -m "add items needed to grow potatoes"
   ```

13. Use a Git command to display a list of the commits. You should see 4!

   ```sh
   git log --oneline
   ```
