# Mission: Improve the School Club Portal

Allow 90–120 minutes. You are contributing to another developer's website. Your work should reach the original project through a pull request.

## 1. Fork and choose where to work

Open https://github.com/Mishael-2584/school-club-portal and click **Fork**. Confirm your copy belongs to your own account. Then choose **Option A or Option B** below. Both options use the same branch, editing, commit, push, and pull request steps.

### Option A: Work on your computer (local repository)

You need Git, a text editor such as Visual Studio Code, a web browser, and an internet connection to clone and push. Python is not required for the local option.

1. Install Git if needed and open a new terminal. Run `git --version` to check it is available.
2. On **your fork**, select **Code → Local → HTTPS** and copy the clone URL.
3. Open a terminal in the folder where you want to store your project. Run the following, replacing `YOUR-USERNAME` with your GitHub username. If you renamed your fork, use its copied URL instead.

```sh
git clone https://github.com/YOUR-USERNAME/school-club-portal.git
cd school-club-portal
git remote -v
```

Confirm `origin` points to **your fork**, so you can push your contribution there.

4. Open this folder in your editor using **File → Open Folder**. If the VS Code command is available, you can also run `code .`.
5. If this is your first time using Git on this computer, set the name and email for commits in this repository. Replace these examples with your own details; you can use your GitHub-provided private commit email from GitHub's email settings.

```sh
git config user.name "Your Name"
git config user.email "YOUR-COMMIT-EMAIL"
```

Keep your terminal in the cloned project folder for the remaining commands. When pushing, complete Git's GitHub sign-in prompt if requested; do not use your GitHub account password as a Git HTTPS password. Cloning your fork gives you a local Git repository; downloading a ZIP does not provide the Git history needed for this exercise.

### Option B: Work in GitHub Codespaces

In your fork, choose **Code → Codespaces → Create codespace on main**. Find the project files in Explorer and open the integrated terminal for the remaining commands.

Before starting, check your account's Codespaces allowance and billing settings. See [Codespaces billing](https://docs.github.com/en/billing/concepts/product-billing/github-codespaces). Select a 2-core machine if available. Stop the Codespace when finished; closing the browser tab alone is not a reliable way to stop it. Stored Codespaces can continue to consume storage allowance.

## 2. Create a branch

```sh
git switch -c improve-school-portal
```

## 3. Improve the website

- Add an Upcoming Events section to `index.html`.
- Add at least two new clubs to `clubs.html`.
- Improve colours and appearance in `style.css`.
- Make the Explore Our Clubs button navigate to the clubs page.
- Add a short description of your contribution to `README.md`.

**Local preview:** Open `index.html` from the cloned folder in your web browser. After saving edits in your editor, refresh the browser. No server or package installation is needed for this HTML/CSS project.

**Codespaces preview:** Run `python3 -m http.server 8000`, then open port 8000 from the Ports panel.

For either option, check both pages, navigation, and a narrow browser window.

## 4. Test .gitignore

Create `.env` in the project root containing only these fictional values:

```dotenv
ADMIN_PASSWORD=school123
API_KEY=example123
```

Create `private-notes.txt` containing fictional practice notes. Then run:

```sh
git status
git check-ignore -v .env private-notes.txt
git ls-files config/.env.example
```

Explain why the first two files do not appear as ordinary untracked changes. The sample `config/.env.example` is already committed: inspect it and keep it tracked. Never use real passwords or keys for this exercise.

## 5. Commit and push

```sh
git status
git add index.html clubs.html style.css README.md
git diff --cached --check
git diff --cached
git commit -m "Improve school club portal"
git push -u origin improve-school-portal
```

Check the staged diff before committing. Confirm neither `.env` nor `private-notes.txt` appears.

## 6. Open a pull request

On GitHub, open your fork and choose **Contribute → Open pull request** or **Compare & pull request**. Set:

- Base repository: `Mishael-2584/school-club-portal`
- Base branch: `main`
- Head repository: your fork
- Compare branch: `improve-school-portal`

Describe your changes, your preview checks, and what you learned about ignored files. Submit the pull request and respond to review feedback.

## 7. Finish

- **Local repository:** Save your files, confirm your contribution is pushed, and close your editor when finished. Keep the cloned folder for future work.
- **Codespaces:** Stop your Codespace from its menu or https://github.com/codespaces. Delete it when no longer needed after confirming your work is pushed.

## Extra challenge: upstream

`origin` normally points to your fork. Add the original repository as `upstream`:

```sh
git remote add upstream https://github.com/Mishael-2584/school-club-portal.git
git remote -v
git fetch upstream
git switch main
git merge upstream/main
git push origin main
```

Finish or commit your current work before switching branches. If `upstream` already exists, inspect it with `git remote -v` instead of adding it again.
