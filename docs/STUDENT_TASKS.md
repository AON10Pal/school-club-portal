# Mission: Improve the School Club Portal

Allow 90–120 minutes. You are contributing to another developer's website. Your work should reach the original project through a pull request.

## 1. Fork and open Codespaces

Open https://github.com/Mishael-2584/school-club-portal and click **Fork**. Confirm your copy belongs to your own account. In your fork, choose **Code → Codespaces → Create codespace on main**. Find the project files in Explorer.

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

Preview with `python3 -m http.server 8000`, then open port 8000 from the Ports panel. Check both pages, navigation, and a narrow browser window.

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

Stop your Codespace from its menu or https://github.com/codespaces. Delete it when no longer needed after confirming your work is pushed.

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
