# Hello World Githooks

## Introduction

This is how you use githooks in a repo

## Contents

- [Setup](#setup)
- [Usage](#usage)

## Setup

Tell this git repo to use your local `.githooks` path:

```bash
git config core.hooksPath .githooks
```

## Usage

Make a commit:

```bash
echo "$(uuidgen)" > uuid.txt
git add .
git commit -m "Committing: $(cat uuid.txt)"
```
