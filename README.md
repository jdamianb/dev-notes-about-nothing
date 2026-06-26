# Dev Notes About Nothing

Personal development notes, experiments, and small technical guides that I want to keep for future reference and share with others.

The idea of this repository is simple: when I learn or configure something useful, I document it in Markdown instead of leaving it only in my shell history, bookmarks, or memory.

## What is inside?

This repository contains practical notes about development tools, Linux setup, Java environments, local agents, and other things I use or test.

Example topics:

* Installing and using SDKMAN on Ubuntu
* Managing multiple Java versions
* Linux development setup notes
* Git and GitHub reminders
* Agent/tooling experiments
* Small troubleshooting guides

## Repository structure

```text
.
├── README.md
├── mkdocs.yml
├── requirements.txt
└── docs/
    ├── index.md
    ├── linux/
    │   └── sdkman-ubuntu.md
    ├── java/
    └── tools/
```

## Requirements

To work with this repository locally, you need:

* Python 3
* Git
* A terminal
* Optionally, a Python virtual environment

## Local setup

Create and activate a virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Install the documentation dependencies:

```bash
pip install -r requirements.txt
```

If `requirements.txt` does not exist yet, install MkDocs manually:

```bash
pip install mkdocs mkdocs-material
```

## Preview the site locally

Run:

```bash
mkdocs serve
```

Then open:

```text
http://127.0.0.1:8000
```

MkDocs will automatically reload the site when Markdown files are modified.

## Add a new note

Create a Markdown file under `docs/`.

Example:

```text
docs/linux/sdkman-ubuntu.md
```

Then add it to the navigation in `mkdocs.yml`:

```yaml
nav:
  - Home: index.md
  - Linux:
      - SDKMAN on Ubuntu: linux/sdkman-ubuntu.md
```

## Build the static site

To generate the static website:

```bash
mkdocs build
```

The generated files are placed in:

```text
site/
```

The `site/` directory is build output and should not be committed to the main branch.

## Deploy to GitHub Pages

Manual deployment:

```bash
mkdocs gh-deploy
```

This publishes the generated site to the `gh-pages` branch.

## Notes style

Each note should try to answer:

* What problem was I trying to solve?
* What commands did I run?
* What worked?
* What failed or was confusing?
* What would I do next time?

A good note is not necessarily perfect. It should be useful to my future self first, and useful to others when possible.

## License

Unless stated otherwise, the notes in this repository are shared for learning and reference purposes.
