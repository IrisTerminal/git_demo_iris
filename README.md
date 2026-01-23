# Data 271 – Git Collaboration Mini Lab

In this activity, you will practice **basic git collaboration** using JupyterHub.

You will:
- clone a repository
- create a branch
- edit a single line in a shared file
- commit your change
- submit your work as a patch file

You do **not** need a GitHub account to complete this activity.

---

## Rules (important!)
- You are assigned **ONE line number** in `lines.txt`
- **Only edit your assigned line**
- Keep your edit to **one sentence**
- Do not change any other lines
- Do not delete line numbers

This mirrors how real data science teams avoid merge conflicts.

---

## Step 1: Open a Terminal in JupyterHub

Go to:
**Files → New → Terminal**

In the terminal, verify git is installed:
```bash
git --version```

## Step 2: Clone the repository
git clone <REPO_URL>
cd data271-git-collab
(Your instructor will give you the exact repo URL.)

## Step 3: Create a branch
Replace X with your assigned line number.
git checkout -b line-X
Example:
git checkout -b line-7

## Step 4: Edit your line
In JupyterHub, click lines.txt
Find your assigned line number
Edit only that line
Save the file
Do not edit any other lines.

## Step 5: Commit your change
git status
git add lines.txt
git commit -m "Edit line X"
Example:
git commit -m "Edit line 7"
## Step 6: Create a patch file
git format-patch -1 HEAD
This creates a file that looks like:
0001-Edit-line-7.patch

## Step 7: Submit your patch
Upload your .patch file to the course submission page as instructed.
Why we are doing this
Git is a core tool for data scientists.
This exercise practices:
careful editing
version control
collaboration without overwriting others’ work
You are learning real-world skills, even with a silly story 🙂
