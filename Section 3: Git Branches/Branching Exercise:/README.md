# Branching Exercise:

1. Make a new folder called Patronus

   ```sh
   mkdir Patronus
   ```

2. Make a new git repo inside the folder (make sure you're not in an existing repo)

   ```sh
   cd Patronus
   git init
   ```

3. Create a new file called patronus.txt (leave it empty for now)

   ```sh
   touch patronus.txt
   ```
   
4. Add and commit the empty file, with the message "add empty patronus file"

   ```sh
   git add patronus.txt
   git commit -m "add empty patronus file"
   ```

5. Immediately make a new branch called harry and another branch called snape (both based on the master branch)

   ```sh
   git branch harry
   git branch snape
   ```

6. Move to the harry branch using the "new" command to change branches.

   ```sh
   git switch harry
   ```

7. In the patronus.txt file, add the following:
   HARRY'S PATRONUS

   /|       |\
`__\\       //__'
   ||      ||
 \__`\     |'__/
   `_\\   //_'
   _.,:---;,._
   \_:     :_/
     |@. .@|
     |     |
     ,\.-./ \
     ;;`-'   `---__________-----.-.
     ;;;                         \_\
     ';;;                         |
      ;    |                      ;
       \   \     \        |      /
        \_, \    /        \     |\
          |';|  |,,,,,,,,/ \    \ \_
          |  |  |           \   /   |
          \  \  |           |  / \  |
           | || |           | |   | |
           | || |           | |   | |
           | || |           | |   | |
           |_||_|           |_|   |_|
          /_//_/           /_/   /_/
   ```sh
   echo "HARRY'S PATRONUS" > patronus.txt
   echo "..." >> patronus.txt
   ```

8. Add and commit the changes, with the commit message "add harry's stag patronus"

   ```sh
   git add patronus.txt
   git commit -m "add harry's stag patronus"
   ```

9. Move over to the snape branch using the "older" command to change branches.

   ```sh
   git switch snape
   ```

10. Put the following text in  the patronus.txt file:
SNAPE'S PATRONUS
                   .     _,
                   |`\__/ /
                   \  . .(
                    | __T|
                   /   |
      _.---======='    |
     //               {}
    `|      ,   ,     {}
     \      /___;    ,'
      ) ,-;`    `\  //
     | / (        ;||
     ||`\\        |||
     ||  \\       |||
     )\   )\      )||
     `"   `"      `""

   ```sh
   echo "SNAPE'S PATRONUS" > patronus.txt
   echo "..." >> patronus.txt  # Add the ASCII art here
   ```

11. Add and commit the changes on the snape branch with the commit message "add snape's doe patronus"

   ```sh
   git add patronus.txt
   git commit -m "add snape's doe patronus"
   ```

12. Next, create a new branch based upon the snape branch called lily

  ```sh
   git branch lily snape
  ```

13. Move to the lily branch

  ```sh
  git switch lily 
  ```

14. Edit the patronus.txt file so that it says LILY'S PATRONUS at the top instead of SNAPE'S PATRONUS (leave the doe ascii-art alone)

  ```sh
  sed -i 's/SNAPE\'S PATRONUS/LILY\'S PATRONUS/' patronus.txt
  ```

15. Add and commit the change with the message "add lily's doe patronus"

  ```sh
  git add patronus.txt
  git commit -m "add lily's doe patronus"
  ```

16. Run a git command to list all branches (you should see 4)

  ```sh
  git branch
  ```

17. Bonus: delete the snape branch (poor Snape)

  ```sh
  git branch -d snape
  ```
