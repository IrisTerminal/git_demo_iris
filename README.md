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

## Directions

- You will edit **one line** in `lines.txt`
- Only edit your assigned line
- You can edit it with whatever flair you wish, but please try to keep it somewhat cohesive with the entire passage
- Please do not edit any other lines
- Do not delete line numbers

This mirrors how real data science teams avoid merge conflicts.

---

## Step 1: Open a Terminal in JupyterHub

Go to:

    Files → New → Terminal

In the terminal, verify git is installed:

    git --version

Then create a signin.

    git config --global user.name "Your Name"
    git config --global user.email "your@email.com"

You can use your real name. The email does not matter. Since we are collaborating, we also want to track who makes what changes.

---

## Step 2: Clone the repository

Run:

    git clone https://github.com/emoochangu/git_demo.git
    cd git_demo

(That is the url of this repo :))

---

## Step 3: Create a branch

Replace X with your assigned line number:

    git checkout -b line-X

Example:

    git checkout -b line-7

---

## Step 4: Edit your assigned line

In JupyterHub:

1. Click `lines.txt`
2. Find your assigned line number
3. Edit **only that line**
4. Save the file

---

## Step 5: Check your git status

Run:

    git status

You should see that `lines.txt` was modified.

---

## Step 6: Commit your change

Run:

    git add lines.txt
    git commit -m "Edit line X"

Example:

    git commit -m "Edit line 7"

---

## Step 7: Create a patch file

Run:

    git format-patch -1 HEAD

This creates a file that looks like:

    0001-Edit-line-7.patch

---

## Step 8: Submit your patch

Upload your `.patch` file to the course submission page as instructed.

---

## Why we are doing this

Git is a standard tool used by data scientists to collaborate safely.

This lab demonstrates how multiple people can work on the same file
**without overwriting each other’s work**, even when not everyone has a
GitHub account.

The story is silly, but the skills are real.
