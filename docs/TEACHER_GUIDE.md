# Teacher guide

## Preparation

Use this repository as the original developer's project. Have students use their own GitHub accounts and forks; they do not need collaborator access to the original. Check Codespaces eligibility, available allowance, and billing settings before class. A local clone and browser can be used if Codespaces is unavailable.

Keep the starter incomplete until students finish their contributions. For repeated classes, preserve a starter branch or use a fresh exercise repository before merging solutions into main.

## Suggested timing (100 minutes)

| Activity | Minutes |
| --- | ---: |
| Fork versus clone | 10 |
| Fork the repository | 10 |
| Open Codespaces | 10 |
| Branch and edit website | 25 |
| Demonstrate .gitignore | 15 |
| Commit and push | 10 |
| Submit pull request | 10 |
| Review and recap | 10 |

## Key explanations

A fork is a repository under the student's GitHub account. A clone is a working copy in a computer or Codespace. Codespaces provides a remote development environment. A push updates the student's fork; a pull request proposes changes to the original repository. A branch keeps the contribution separate from main.

`.gitignore` applies to untracked files; it does not untrack files already committed. Demonstrate `git check-ignore -v .env private-notes.txt`. The committed `.env.example` is a safe template. Ignore rules are not a security system and cannot undo exposure of a committed secret. Use fictional values throughout this lesson.

## Review checklist

- The pull request comes from the student's fork and contribution branch.
- The home page includes upcoming events.
- At least two additional clubs appear.
- Styling has been improved and both pages remain usable on a narrow screen.
- Navigation and the Explore link work.
- The README describes the contribution.
- Private notes and environment values are absent from the diff.
- The sample environment file remains tracked.
- The student explains their checks and can respond to feedback.

## Assessment questions

1. Does a fork grant write access to the original repository?
2. How does a fork differ from a clone?
3. Where does a Codespace run?
4. Does closing the browser reliably stop it?
5. Why ignore local environment files?
6. What if a file was tracked before being added to .gitignore?
7. What do origin and upstream refer to?
8. Does pushing to a fork change the original?
9. What does a pull request propose?
10. Why work on a separate branch?

## Official references

- [Fork a repository](https://docs.github.com/en/get-started/quickstart/fork-a-repo)
- [Codespaces quickstart](https://docs.github.com/en/codespaces/quickstart)
- [Ignoring files](https://docs.github.com/en/get-started/getting-started-with-git/ignoring-files)
- [Codespaces billing](https://docs.github.com/en/billing/concepts/product-billing/github-codespaces)
