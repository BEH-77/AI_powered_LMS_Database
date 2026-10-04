# Contributing

This is how we work with GitHub in this project. Please follow these steps every time.

## First time only

Clone the repository and go into the folder:

```bash
git clone https://github.com/BEH-77/AI_powered_LMS_Database.git
cd AI_powered_LMS_Database
```

## Before starting any change

Switch to `main` and make sure your local copy is up to date:

```bash
git checkout main
git pull
```

## Making a change

Never work directly on `main`. Create your own branch and work in it:

```bash
git switch -c yourname/short_description
```

Name your branch with your name, a slash, and a short description of the change. For example: `badr/add_student_table`.

Test your code on your computer before pushing it.

## Saving and pushing your work

```bash
git add .
git commit -m "Short description of what you changed"
git push -u origin yourname/short_description
```

The `-u` is only needed the first time you push a new branch. After that, `git push` is enough.

## Opening a pull request

1. Go to the repository on GitHub.
2. Click "Compare & pull request" for your branch.
3. Write a short description of what you changed and why.
4. Ask a teammate to review it.
5. Once it is approved, merge it into `main`.

## The ERD

The ERD is generated automatically when changes to a `.puml` file are merged into `main`. To change the diagram:

- Edit `docs/erd.puml`, never `docs/erd.png`. The bot overwrites the image.
- Optional: preview it locally with `java -jar tools/plantuml.jar -tpng docs/erd.puml`.
- After your pull request is merged, wait about a minute. A new commit called "Update ERD" will appear on `main`.

## After your pull request is merged

Update your local copy so you have the latest code and the new ERD:

```bash
git checkout main
git pull
```

## Rules

- Always run `git pull` on `main` before creating a new branch.
- One branch per change, and keep branches small.
- Do not commit passwords, tokens, or `.env` files.
- If a push is rejected, run `git pull` and try again.
- If you get a merge conflict, ask for help before deleting anything.