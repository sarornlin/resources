# Introduction

This document will cover different Git commands, common practices, and recommendations on how to write Git messages.

When writing your message, start off with:

**If applied, this commit will... _\<commit subject>_**

---

# Opening Pull Request

```bash
#Be on your branch
git checkout -b MY-BRANCH-NAME

#Make commits
git status                          #View Pending Changes
git add -A                          #Add all changes
git commit -m 'meaningful message'  #Commit changes

#Switch to main
git checkout main

#Pull (Fetch & Merge) from remote Main
git pull origin main

#Switch back to your branch
git checkout MY-BRANCH-NAME

#Merge with local main
git merge main

#Time to resolve any conflicts! Use Visual Studio to compare differences.

#Push to Server
git push origin HEAD

#Time to Open a PR!
```

---

# Making Git Commit Messages

## Guidelines

### Ask Yourself:

Think of the What's and Why's:

-   Why have I made these changes?
-   What effect have my changes made?
-   Why was the change needed?
-   What are the changes in reference to?

Make it so your future self or any other person can understand it.

```bash
git commit -m 'Add margin'

VS

git commit -m 'Add margin to nav items to prevent them from overlapping the logo'
```

The title is like a news article headline. Sum up what happened and what is important. Then write further details in body in an organized fashion.

### DO

-   **Commit often** to make checkpoints along the code to go back to if needed.
-   **Write in imperative:** "Fix bug" and not "Fixed bugs" or "Fixes bug". Imperative mood gives the tone you are giving an order or request.
-   Further paragraphs come after blank lines. Bullet points are okay. Hyphen or asterisk is used for bullet.
-   Use the body to explain what and why you have done something. You can leave out details on how it was done.
-   Include bug number if relevant.
-   Does not need to explain everything in detail
-   First line < 50 characters, body < 72 characters

### DO NOT

-   End the subject line with a period

-   Assume the reader understands what the original problem was

-   Assume that the code is self-evident/self-documenting

## Commit Subject Line

A properly formed subject line should always complete the following sentence:

> If applied, this commit will \<_your subject line here_>

## Example for commit message

```
Add CPU arch filter for scheduler support
In a mixed environment of...
```

```markdown
If applied, this commit will...
...Create ProfileNav.jsx component
...Add mapLists mapping function to ProfileNav.jsx
...Remove sideNavBar.jsx file
...Update profilenav.css name to fit naming convention
...Update Profile.jsx to use ProfileNav component
...Refactor ConnectedAccount.jsx by removing excess comments
```

## Anatomy

### Basic

```bash
git commit -m <message>
```

### Detailed

```bash
git commit -m <title> -m <description>
```

## Commit Verbs

-   Add: create a capability e.g. feature, test, dependency
-   Remove: remove a capability
-   Fix: fix an issue e.g. bug, typo, accident, misstatement
-   Refactor: a code change that MUST be just a refactoring
-   Reformat: refactor off ormatting, e.g. omit whitespace
-   Optimise: refactor of performance, e.g. speed up code
-   Update: changing code where its a mix of things
-   Implement: a form of add
-   Change: remove and add capability
-   Use
-   Set
-   Rename: renaming a file or function/method name
-   Modify:

---

# Sources

[Githut Robertpainsi: Commit Message Guidelines](https://gist.github.com/robertpainsi/b632364184e70900af4ab688decf6f53)

[Freecodecamp](https://www.freecodecamp.org/news/how-to-write-better-git-commit-messages/)

[Knowbl](https://github.com/knowbl/git-commit-message)

[CBeams: How to Write a Git Commit Message](https://cbea.ms/git-commit/)
