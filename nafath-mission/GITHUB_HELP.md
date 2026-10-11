# GitHub Guide for the Nafath Mission

You can complete the mission in two ways. Choose one:

- **Option A: Browser only.** No installation. Recommended if you are new to Git.
- **Option B: Git on your computer.** For those who already use Git or want to learn it.

Both give the same result. We check your repository's **commit history**.
You may also switch from Option B to Option A at any time in the same repository.

All work is done on the **main** branch. Do not create other branches.

---

## Part 1: Create your GitHub account (everyone)

1. Go to https://github.com/signup
2. Enter your email, create a password and choose a username.
   Use a professional username (for example your first name and a word),
   not your phone number or national ID.
3. Complete the verification step and enter the code sent to your email.
4. Recommended: go to **Settings > Emails** and tick
   **"Keep my email addresses private"**. This hides your email in your commits.

## Part 2: Create your public repository (everyone)

1. Sign in. Click the **+** icon at the top right, then **New repository**.
2. Repository name: `nafath-brief` (exactly, lowercase).
3. Select **Public**.
4. Tick **"Add a README file"**.
5. Click **Create repository**.

You now have a repository with one file, `README.md`.
**Do not edit README.md at any point.**

---

## Option A: Complete the mission in the browser

### A1. Create a new file

1. In your repository, click **Add file > Create new file**.
2. In the name box, type the file name (for example `brief.md`).
3. Type or paste the content into the editor.
4. Click **Commit changes...** (green button, top right).
5. In the dialog, delete the default message and type the **exact** commit
   message for the step (for example `skeleton: NAFATH-V1`).
6. Make sure **"Commit directly to the main branch"** is selected.
7. Click **Commit changes**.

### A2. Edit an existing file

1. Click `brief.md` to open it.
2. Click the **pencil icon** ("Edit this file").
3. Make only the change required for the current step.
4. Click **Commit changes...**, type the exact message for the step,
   keep **"Commit directly to the main branch"** selected,
   and click **Commit changes**.

One step = one commit. Repeat for every step.

### A3. Check your work

Click `brief.md` and use the **Preview** tab while editing, or open the file
after committing, to see how it looks.

### A4. Find your commit IDs (needed for the last step)

1. On your repository's main page, click the **Commits** link
   (clock icon, above the file list, showing the number of commits).
2. Each commit shows a short ID of 7 characters (for example `1a2b3c4`).
   Click the copy icon next to it to copy it.
3. The list shows the **newest commit first**.
   In `CHANGELOG.md` you must write them **oldest first**.

---

## Option B: Use Git on your computer

### B1. Install Git

- **Windows:** download and install Git for Windows from
  https://git-scm.com/download/win (keep the default options).
  It includes Git Bash and a sign-in helper.
- **macOS:** open Terminal and type `git --version`.
  If Git is not installed, macOS offers to install it. Accept.
- **Linux (Ubuntu/Debian):** run `sudo apt install git`

Check that it works:

```
git --version
```

### B2. Tell Git who you are

Use your GitHub username and your private GitHub email.
You can find the private email in GitHub **Settings > Emails**;
it ends with `@users.noreply.github.com`.

```
git config --global user.name "your-username"
git config --global user.email "12345678+your-username@users.noreply.github.com"
```

### B3. Copy your repository to your computer

Create the repository in the browser first (Part 2). Then run:

```
git clone https://github.com/your-username/nafath-brief.git
cd nafath-brief
```

This downloads your repository and connects it to GitHub.
To confirm the connection, run:

```
git remote -v
```

You should see `origin` pointing to your `nafath-brief` repository.

### B4. Make each step as one commit

Edit `brief.md` in any text editor (VS Code, Notepad, TextEdit), save it, then run:

```
git add brief.md
git commit -m "skeleton: NAFATH-V1"
git push origin main
```

Repeat for each step, using that step's exact commit message.
For the last step, use `git add CHANGELOG.md`.

### B5. Sign in when you push

- **Windows:** the first time you push, a browser window opens.
  Sign in to GitHub and approve.
- **macOS and Linux:** GitHub does not accept your account password here.
  Create a personal access token instead:
  1. In GitHub, go to **Settings > Developer settings > Personal access tokens >
     Fine-grained tokens > Generate new token**.
  2. Repository access: **Only select repositories > nafath-brief**.
  3. Permissions: **Contents > Read and write**.
  4. Click **Generate token** and copy it. You will not see it again.
  5. When Git asks for your password, paste the token.

### B6. Find your commit IDs

```
git log --oneline
```

The newest commit is at the top. Write them in `CHANGELOG.md` **oldest first**.

### B7. Important rules for Option B

- Add only the file the step needs (`git add brief.md`), not `git add .`,
  so no hidden system files are committed.
- After pushing, **never** use `git commit --amend`, `git rebase`
  or `git push --force`. These rewrite history and change your commit IDs.
- After pushing, open your repository in the browser and confirm
  every commit is there.

---

## Before you submit

Open your repository in a **private / incognito browser window** (not signed in).
Confirm that you can see `brief.md`, `CHANGELOG.md` and all your commits.
If you cannot see them, your repository is not public.

## If something goes wrong

- **Wrong content or a typo in a step:** make an extra commit with the message
  `fix: <short description>`, for example `fix: correct resource link in data`.
  Extra `fix:` commits are allowed.
- **Wrong commit message:** do not rewrite history. Continue with the next steps.
  Mention it in the form's "difficulties" question.
- **Committed to the wrong file or deleted something:** restore it with a
  `fix:` commit.
- **Still stuck:** contact [support email] before the deadline.
