# 🌀 Merge Tutorial

Generating merge conflicts and learning to solve them

---

## 📋 Step-by-Step Instructions

### 1. Open a New Folder on Your Device
Navigate to the location where you want to create your project:

```bash
cd path/to/your/folder
```

### 2. Create a New File Named `notes.txt`
In that folder, create a file called `notes.txt` and write a simple list in it, for example:

```
GROCERY LIST

banana  
mango  
papaya  
cereal  
```

### 3. Initialize Git
Start version control in the current folder:

```bash
git init
```

### 4. Commit the Initial List
Stage and commit your initial list:

```bash
git add .
git commit -m "initial commit with grocery list"
```

### 5. Create a New Branch (to Generate Merge Conflicts)
Create and switch to a new branch:

```bash
git checkout -b test
```

### 6. Change Something in the List
In the `test` branch, edit `notes.txt`. For example, delete an item or rename one:
- Rename `cereal` to `granola`
- Or remove `banana`

### 7. Add and Commit the Changes

```bash
git add .
git commit -m "update branch test"
```

### 8. Switch Back to the Main Branch

```bash
git checkout main
```

Now make a **different** change in `notes.txt`, ideally to the same lines (e.g., rename `papaya` to `pineapple`).

### 9. Commit the Changes in Main

```bash
git add .
git commit -m "update on main branch"
```

### 10. Merge the `test` Branch into `main`

```bash
git merge test
```

💥 You’ll likely see a **merge conflict**. Open `notes.txt` and resolve the conflict manually.

Conflict markers will look like this:

```plaintext
<<<<<<< HEAD
pineapple
=======
papaya
>>>>>>> test
```

Decide whether to keep:
- The change from `main` (`HEAD`)
- The change from `test` (`incoming`)
- Or combine both

Then save the file.

### 11. Finalize the Merge

After resolving the conflict, stage and commit the final version:

```bash
git add .
git commit -m "resolved merge conflict"
```

---

## ✅ That’s It!

You've now created and resolved a Git merge conflict.  
Great job — you're one step closer to being a Git pro! 🚀
