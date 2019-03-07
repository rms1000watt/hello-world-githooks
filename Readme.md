# Hello World Githooks

## Introduction

This is how you use githooks in a repo

## Contents

- [Setup](#setup)
- [Usage](#usage)
- [Other Hooks](#other-hooks)

## Setup

Tell this git repo to use your local `.githooks` path:

```bash
git config core.hooksPath .githooks
chmod -R a+x .githooks
```

**Every dev has to run this ^^^ on their machine**

## Usage

Make a commit:

```bash
echo "$(uuidgen)" > uuid.txt
git add .
git commit -m "Committing: $(cat uuid.txt)"
```

Then you should see the text in `.githooks/pre-commit` appear.

## Other Hooks

You can create other hooks. Create another file with one of these names and they will occur at a particular time. They have to be named like:

```bash
- applypatch-msg
- commit-msg
- fsmonitor-watchman
- post-update
- pre-applypatch
- pre-commit
- pre-push
- pre-rebase
- pre-receive
- prepare-commit-msg
- update
```
