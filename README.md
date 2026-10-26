# School Club Community Portal

A beginner HTML and CSS contribution project: **Fork, Code, Ignore and Collaborate**.

This starter website helps students discover school clubs. It intentionally leaves work for a student contributor: upcoming events, more clubs, and visual improvements.

## Start the lesson

1. Sign in to your own student GitHub account.
2. Fork [Mishael-2584/school-club-portal](https://github.com/Mishael-2584/school-club-portal).
3. Choose to clone your fork onto your computer **or** open it in GitHub Codespaces.
4. Follow the [student task sheet](docs/STUDENT_TASKS.md), which includes setup instructions for both options.

The student needs a different GitHub account from the original repository owner to practise this fork workflow.

## Run the website

Locally, open `index.html` in a browser. No packages or build step are required.

In Codespaces, run:

```sh
python3 -m http.server 8000
```

Open port **8000** from the Ports panel. Keep the forwarded port private. Stop the server with Ctrl+C.

## Project files

- `index.html`: home page; upcoming events are a student task.
- `clubs.html`: two starter clubs; add at least two more.
- `style.css`: starter appearance for students to improve.
- `.gitignore`: excludes local configuration, notes, and temporary files.
- `config/.env.example`: safe sample configuration; this static website does not load environment files.
- [Teacher guide](docs/TEACHER_GUIDE.md): timing, assessment, and review checklist.

## Contributing

Follow the task sheet, work on a separate branch in your fork, and open a pull request against this repository's `main` branch. Describe your changes and how you checked them. Use only fictional data in configuration exercises.

## License

MIT; see [LICENSE](LICENSE).
