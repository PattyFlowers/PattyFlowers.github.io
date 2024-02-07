---
layout: post
title:  "Pre-commit git hooks"
date:   2024-02-07
categories: Programming
tags: ["programming", "coding", "software development", "tech"]
---

# Pre-commit git hooks

Sometimes, we may need to run our services locally with a series of properties that we don't want to accidentally commit to our repositories for being sensitive. Whilst looking for a 
solution to this problem, I came accross git's hooks, and more particularly, pre-commit hooks. I know other people use them, for example, to make sure all of their commits are signed, and I
can only imagine how many other uses they may have.

Today, I would like to share with you, in an easy way, how to use them.

Steps:
1. First, you will need to decide if you'd like to keep these hooks to yourself or they will be committed and shared along the rest of the repo.
  * **Local-only:** Find the `.git/hooks` folder at the root of your repo (it will likely be hidden) and create a file called `pre-commit`, without any extensions. Make the file executable by 
  running `chmod + x .git/hooks/pre-commit` from the root of your project. The `.git` folder is by default ignored by git and therefore, any changes you make inside it will only affect your local project.
  * **Committed to repo:** Create a new folder called `.githooks` (or anything you like, but we'll use this as an example) and create a file called `pre-commit` inside it, without any extensions. 
  Run the following command: `git config --local core.hookspath .githooks/` to change where git looks for the hooks (make sure that you are not using any other hooks inside the `.git` folder, as this 
  will change the configuration). If needed, you can also check where this configuration is pointing to by running `git config -l` and looking for the `core.hookspath` line, if it is not present, it 
  defaults to `.git`. The folder and file we created can be commited later on if needed.

2. Inside our `pre-commit` file, we will add the following script, which finds the files that have been staged in git, iterates through them and looks for a FORBIDDEN_STRING. If found, it aborts
the commit and displays an error message that includes the name of the problematic file:

```
#!/bin/sh
FORBIDDEN_STRING="FORBIDDEN_STRING"

# Get a list of the modified files
FILES=$(git diff --cached --names-only)
for FILE in $FILES
  do
    if grep -q "$FORBIDDEN_STRING" $FILE
    then
      echo "Before committing, you must remove the added properties in the following file: $FILE"
      exit 1
  fi
done

```
3. If you decided to commit the pre-commit hook to the repository, your colleagues would need to run the command `git config --local core.hookspath .githooks/` to activate this feature.

And that is all for now, I hope you found it helpful and please let me know if you have any questions or feedback. See you soon, catonauts!


 <p><img src="/assets/images/trophy-technology-CiYaInyTvwU-unsplash.jpg" alt="Hand holding a fishing lure" width="300"></p>
