# merge_tutorial
Generating merge conflicts and learning to solve them  

# 1. Open a new folder in your local device
 cd .. to that folder
# 2. Open a new file in that folder called:
notes.txt
# 3. Write a list of something else, example:
GROCERY LIST

banana
mango
papaya
cereal

# 4. Initialise Git
git init

# 5. Create a new branch (to generate merge problems)
git checkout -b test

# 6. Change something in the current list: delete or rename an item

# 7. Add and commit the changes
git add . && git commit -m "update branch test"

# 8. Switch back to the main branch
git checkout main

# 9. Check the status and hopefully find a merge problem
git status

# 10. Resolve merge conflicts choosing which entry should stay : main ? incoming ? both

# 11. Add and commit changes using the commands in point 7

