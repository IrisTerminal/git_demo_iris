# Data 271 – Git Collaboration Mini Lab (GitHub Pull Request Version)

In this activity, you will practice basic git collaboration using GitHub.

You will:
- fork a repository
- clone your fork in JupyterHub
- create a branch
- edit a single line in a shared file
- commit your change
- push your branch to GitHub
- open a Pull Request (PR) so the instructor can merge it live on the projector

---

## Rules (important!)

- You are assigned ONE line number in lines.txt
- Only edit your assigned line
- Keep your edit to one sentence
- Do not change any other lines
- Do not delete line numbers

This mirrors how real data science teams avoid merge conflicts.

---

## Step 1: Create a GitHub account (if needed)

If you do not already have a GitHub account, create one now.

---

## Step 2: Fork the class repository

Open the class repository in your browser:

    https://github.com/emoochangu/git_demo

Click:

    Fork

This creates your own copy, for example:

    https://github.com/YOUR_GITHUB_USERNAME/git_demo

---

## Step 3: Open a Terminal in JupyterHub

In JupyterHub:

    Files → New → Terminal

Verify git is installed:

    git --version

---

## Step 4: Configure your Git identity (one time only)

Git requires a name and email to create commits.

Run:

    git config --global user.name "Your Name"
    git config --global user.email "your@email.com"

Notes:
- Use your real name.
- The email does NOT need to be your GitHub email.
- This does not send email. It is just stored in your commit history.

(Optional check):

    git config --global --list

---

## Step 5: Clone YOUR fork (not the instructor repo)

Replace YOUR_GITHUB_USERNAME with your GitHub username:

    git clone https://github.com/YOUR_GITHUB_USERNAME/git_demo.git
    cd git_demo

Confirm you see the files:

    ls

You should see:

    README.md
    lines.txt

---

## Step 6: Create a branch for your assigned line

Replace X with your assigned line number:

    git checkout -b line-X

Example:

    git checkout -b line-7

(Optional check):

    git branch

---

## Step 7: Edit ONLY your assigned line

In JupyterHub:
1. Click lines.txt
2. Find your assigned line number
3. Edit ONLY that line
4. Save the file

Confirm git sees your change:

    git status

---

## Step 8: Commit your change

Stage and commit:

    git add lines.txt
    git commit -m "Edit line X"

Example:

    git commit -m "Edit line 7"

(Optional check):

    git log --oneline -5

---

## Step 9: Push your branch to GitHub

Push your branch:

    git push -u origin line-X

Example:

    git push -u origin line-7

IMPORTANT:
- GitHub may ask you to sign in.
- GitHub does NOT accept passwords for terminal git pushes.
- If prompted for a password, you must use a Personal Access Token (PAT) instead.

If pushing from the terminal is difficult today:
- You can still complete the lab using the “Browser Option” below.

---

## Step 10: Open a Pull Request (PR)

Go to your fork on GitHub:

    https://github.com/YOUR_GITHUB_USERNAME/git_demo

Click:
- Pull requests
- New pull request

Set:
- Base repository: emoochangu/git_demo
- Base branch: main
- Compare branch: your line-X branch

Submit the Pull Request.

Your instructor will review PRs on the projector and merge them.

---

## Browser Option (if terminal push is difficult)

If you cannot push from the terminal, do this instead:

1. Go to your fork on GitHub:
       https://github.com/YOUR_GITHUB_USERNAME/git_demo

2. Click lines.txt

3. Click the pencil icon to edit

4. Edit ONLY your assigned line

5. When committing on GitHub, choose:
       Create a new branch for this commit

6. Click:
       Propose changes

7. Open the Pull Request

This still achieves the main learning goal: collaboration through Pull Requests.

---

## Why we are doing this

Git is a standard tool used by data scientists to collaborate safely.

Pull Requests make it possible for many people to work on the same project without overwriting each other’s work.

The story is silly, but the skills are real.
